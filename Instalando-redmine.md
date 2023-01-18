￼
## Instalando um servidor RedMine de forma fácil pelo Docker

Recentemente publiquei no LinkedIn um tutorial de como instalar facilmente o Testlink, que é um gerenciador de Bugs, para continuar, influenciado pela necessidade de exercitar o uso do Redmine, que também é uma ferramenta Opensource para gerenciamento de Bugs estou disponibilizando este tutorial para a instalação do Redmine em seu computador ou servidor.
É necessário ter o [Docker](https://www.docker.com) instalado para iniciar.

- Crie uma rede no docker  

```
	docker network create redmine-net

```Para melhor segurança


- Instale o mySQL  
```
docker run -d --name some-mysql --network some-network -e MYSQL_USER=redmine -e MYSQL_PASSWORD=secret -e MYSQL_DATABASE=redmine -e MYSQL_RANDOM_ROOT_PASSWORD=1 mysql:5.7
```- Instale o Redmine  
- Use  
