Change nginx file for laravel public folder path

For Laravel: root /var/www/public;

Other: root /var/www;

/var/www -> Path of working directory

## Before using docker, Please make sure docker is installed in your system/machine
Command for checking docker version: docker -v


## Project setup guide

1. clone project in your specific drive or directory
1. Install docker and docker compose in your machine
2. Open power shell
3. Navigate to your project directory, reffer step 1.
4. docker-compose up -d

## Run commands in specific container
docker-compose exec app nano .env

Explanation 

docker-compose exec : This command to execute commands
app : this is container name, In which we want to run command 
nano .env : This is command this can be php artisan migrate or anything.

## Stop all container
docker-compose down
## Start all required containers
docker-compose up -d

-d : Run the container in background
## Accessing MySql
1. docker-compose exec db bash
2. After entering db bash hit 
    mysql -u root -p
for mysql root password and and default database reffer docker-compose.yml file

## For setting Nginx Server
1. please configure ports in docker-compose.yml file under nginx service

## For Nginx, MySql and PHP settings please have a look on docker-compose.yml and dockerfile.

## Project contains seprate configuration files under project i.e php, mysql, nginx folder