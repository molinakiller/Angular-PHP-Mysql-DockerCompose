# ==This project has been developed on **Ubuntu 18**==

CRUD with PHP-Mysql inside of Docker Compose as backend and Angular 9 as frontend.

# ==This project has been developed with this **Versions**== 

+ **Docker version: 19.03.9**

+ **Docker-compose version: 1.21.2**

- **Angular version: Angular/Cli 9.1.6**

- **Node version: 12.16.3**


This project can be run by **any** operative system because it use Docker.

#       ==REQUIREMENTS==

1. Any operative system with **GUI**

2. Install **Docker** and **Docker-compose** = [SHOW HOW](https://github.com/molinakiller/Angular-PHP-Mysql-DockerCompose/blob/master/Docker/readme.MD)

3. Install **node.js** and **Angular/Cli** = [SHOW HOW](https://github.com/molinakiller/Angular-PHP-Mysql-DockerCompose/blob/master/README.md)

4. Install Mysql-client 5.6

5. Check the environment config in:

- PHP_API_SERVER IP CONTAINER = [SHOW CONF](https://github.com/molinakiller/Angular-PHP-Mysql-DockerCompose/blob/master/Angular/src/app/api.service.ts)

- Mysql USER CONF docker-compose = [SHOW CONF](https://github.com/molinakiller/Angular-PHP-Mysql-DockerCompose/blob/master/Docker/docker-compose.yml)

- Mysql-Server IP and USER OF CONTAINER = [SHOW CONF](https://github.com/molinakiller/Angular-PHP-Mysql-DockerCompose/blob/master/Docker/backend/api.php)

- Mysql-Server IP and USER OF CONTAINER X2 = [SHOW CONF](https://github.com/molinakiller/Angular-PHP-Mysql-DockerCompose/blob/master/Docker/backend/index.php)

- Mysql-Server IP and USER OF CONTAINER X3 = [SHOW CONF](https://github.com/molinakiller/Angular-PHP-Mysql-DockerCompose/blob/master/Docker/backend/api/database.php)

# ==RUN==

**START APACHE-PHP AND MYSQL-SERVER SERVER BACKEND WITH DOCKERCOMPOSE**

$cd Angular-PHP-Mysql-DockerCompose

$cd Docker

$sudo docker-compose **build**

$sudo docker-compose up

**CREATE TABLE ON MYSQL SERVER**

$sudo mysql -u root -proot -h 172.18.0.2

mysql->use mydb;

mysql->create table policies( id int not null auto_increment, number varchar(20), amount float, primary key(id)); 

mysql->exit;

**START ANGULAR FRONTEND**

$cd Angular

$sudo npm install

$sudo ng serve

Go to http://localhost:4200/dashboard
