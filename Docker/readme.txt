# == INSTALL DOCKER ON UBUNTU 18 ==

$apt get update

$sudo apt install apt-transport-https ca-certificates curl software-properties-common

$curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

$sudo apt update

$sudo apt install docker-ce

$sudo systemctl status docker

# == INSTALL DOCKER COMPOSE ON UBUNTU 18 ==

$sudo curl -L "https://github.com/docker/compose/releases/download/1.25.5/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose

$sudo chmod +x /usr/local/bin/docker-compose

# == ADMIN DOCKER ==

Show containers running --> **$sudo docker ps** 

Show container info --> **$sudo docker inspect [container_id]**

Show containers images --> **$sudo docker images**

Display networks --> **$sudo docker network ls**  

Display detailed network information --> **$sudo docker network inspect [network_id]**  

Remove container --> **$sudo docker rm [container_id]**

Remove images --> **$sudo docker rmi [image_id]**

# == ADMIN DOCKER COMPOSE ==

Generate containers with docker-compose--> **$sudo docker-compose build**

Run containers with docker-compose--> **$sudo docker-compose up**

Stop containers with docker-compose--> **$sudo docker-compose stop**
