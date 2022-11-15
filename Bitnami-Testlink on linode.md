# Bitnami/Testlink on linode
#### Testlink
#### Tutorial de como rodar o Testlink no Linode.

A princípio o desafio era colocar o TestLink acessível a todos da equipe então fazer a instalação em um servidor de host web que tenho com Mariadb 10.3.36 e PHP 7.4.3 e o resultado foi sempre erro de autenticação genérico com banco de dados, tanto Mysql como Postgre, isso foi, utilizando os arquivos baixados do GitHub do projeto oficial.

Tentei fazer a instalação local conforme alguns vídeos da internet utilizando instalação local com servidor Mamp Apache Php 7 e mysql 8.0.31 também sem sucesso com outro erro genérico de autenticação de banco de dados, nenhum dos erros gerou log na pasta devida nem explicava exatamente qual o erro.

O projeto do Testlink está sem atualização oficial desde em 2018, mas sem novas versões, provavelmente já não suporta alguns comandos mais recentes.

Por final decidi baixar o espelho de Docker da Bitnami já abandonado e coloquei no Linode.

1. Crie uma conta no  Linode, a conta vem com 100 dólares de crédito.

2. Crie uma máquina virtual no Linode, seguindo este passo a passo:
 [https://scribehow.com/shared/Linode_basico__VKDaQ8dSQla3hIZOMct0Ag]

3. No painel de controle do Linode, anote os dados de ip address v4, v6 e acesso ssh\
[Imagem de menu do Linode](/Bitnami-Testlink%20on%20linode/ilustracao-painel-controle.png)

4. Acesse o ssh pelo comando citado acima ou pelo Linode Shell no botão Launch LISH console.

5. Aguarde a máquina virtual terminar de fazer o boot e configure o sistema:

6. Configure o horário local:\
`timedatectl set-timezone ‘America/Sao_Paulo’`

7. Configure o hostname, pode ser qualquer coisa, eu optei usar testlinkhost
`hostnamectl set-hostname testlinkhost `

8. Edite o arquivo de configuração do servidor com o comando
`nano /etc/hosts`

9. Na parte de cima de hosts ipv4 adicione
`<ip que voce copiou do dashboard do Linode>.  Testlinkhost`

10. Na parte de baixo onde é ipv6 faça a mesma coisa, cole o ipv6 que você pegou do Linode
`<ip que voce copiou do dashboard do Linode>.  Testlinkhost`

11. Aperte <ctrl-x> e salve

12. Instale o docker: (atenção que as urls estão configuradas para Debian, pois foi esse linode selecionado)
```
sudo apt remove docker docker-engine  [docker.io](http://docker.io) 
sudo apt update
sudo apt install apt-transport-https ca-certificates curl gnupg lsb-release
sudo mkdir -p /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/debian/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
echo “deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/debian $(lsb_release -cs) stable” | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo chmod a+r /etc/apt/keyrings/docker.gpg
sudo apt-get update
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin 
sudo systemctl start docker
sudo docker run hello-world
```
	
	Se você receber essa mensagem Hello from Docker!
	This message shows that your installation appears to be working correctly., você conseguiu instalar o docker.

13. Instale um servidor de Mysql, nesse caso usei o MariaDB, o primeiro comando é para listar os pacotes possíveis, veja se há um mariadb na lista ou se ele possui alguma versão e anote.
```
docker search mariadb
docker pull mariadb
```

14. Rode o Mariadb
`docker run --name mariadbtest -e MYSQL_ROOT_PASSWORD=mypass -p 3306:3306 -d docker.io/library/mariadb`

15. Baixe o testlink da Bitnami
```
docker pull bitnami/testlink:latest
curl -sSL https://raw.githubusercontent.com/bitnami/bitnami-docker-testlink/master/docker-compose.yml > docker-compose.yml
```

16. Crie uma rede no Docker
`docker network create testlink-network`

17. Crie um volume de container para o MariaDB
```
docker volume create --name mariadb_data
docker run -d --name mariadb \
  --env ALLOW_EMPTY_PASSWORD=yes \
  --env MARIADB_USER=bn_testlink \
  --env MARIADB_PASSWORD=bitnami \
  --env MARIADB_DATABASE=bitnami_testlink \
  --network testlink-network \
  --volume mariadb_data:/bitnami/mariadb \
  bitnami/mariadb:latest
```

18. Crie um volume de container para o testlink
```
docker volume create --name testlink_data
docker run -d --name testlink \
  -p 8080:8080 -p 8443:8443 \
  --env ALLOW_EMPTY_PASSWORD=yes \
  --env TESTLINK_DATABASE_USER=bn_testlink \
  --env TESTLINK_DATABASE_PASSWORD=bitnami \
  --env TESTLINK_DATABASE_NAME=bitnami_testlink \
  --network testlink-network \
  --volume testlink_data:/bitnami/testlink \
  bitnami/testlink:latest
```

Acesse o site através do ip porta 8080

Obs.: Caso ele pedir um servidor válido SMTP para criar usuário, adicione na linha de comando do container do testlink:
 —env TESTLINK_SMTP_HOST=<servidor>
 —env TESTLINK_SMTP_PORT=<porta>
 —env TESTLINK_SMTP_USER=<login>
 —env TESTLINK_SMTP_PASSWORD=<senha>

---
**Referências:**
 [https://github.com/bitnami/bitnami-docker-mariadb](https://github.com/bitnami/bitnami-docker-mariadb)
  
 [https://hub.docker.com/r/bitnami/testlink](https://hub.docker.com/r/bitnami/testlink) 
 
 [https://github.com/TestLinkOpenSourceTRMS/testlink-code](https://github.com/TestLinkOpenSourceTRMS/testlink-code) 
 
 [https://www.linode.com/docs/guides/installing-and-using-docker-on-ubuntu-and-debian/](https://www.linode.com/docs/guides/installing-and-using-docker-on-ubuntu-and-debian/) 
 
 [https://www.linode.com/docs/guides/what-is-docker/](https://www.linode.com/docs/guides/what-is-docker/) 

https://mariadb.com/kb/en/installing-and-using-mariadb-via-docker/

https://cloud.linode.com/linodes/40031519
