#!/bin/bash

# Stop and remove existing containers
docker stop node-container php-container mysql-container || true
docker rm node-container php-container mysql-container || true

# Pull the latest Docker images
docker pull omerpeled13/super-app:node
docker pull omerpeled13/super-app:php
docker pull omerpeled13/super-app:mysql

# Run the Docker containers
docker run -d --name mysql-container -e MYSQL_ROOT_PASSWORD=password -e MYSQL_DATABASE=super-app -p 3306:3306 omerpeled13/super-app:mysql
docker run -d --name node-container -p 3000:3000 yomerpeled13/super-app:node
docker run -d --name php-container -p 80:80 omerpeled13/super-app:php
