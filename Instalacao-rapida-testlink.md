
# Instalação rápida do Testlink
[Logo Testlink](https://dsc.cloud/599510/1-ezeaO1L6xMh55p00csxPfw.png "")<!-- {"preview":"true"} -->
Para aqueles colegas que participaram do grupo e do #PTQS e tiverem interesse em instalar o Testlink de forma fácil em sua máquina ou servidor, vou postar aqui dois comandos que fazem o truque.
docker run -d --name mariadb 

docker run -d --name testlink   --publish 8080:8080    

E por final montaremos o container do testlink dentro do volume testlink_data, baixando a última imagem automaticamente do repositório da Bitnami e estará dentro da rede interna rede-docker para se comunicar com o mariaDB.

Para listar todos os containers configurados no seu Docker utilize o comando: