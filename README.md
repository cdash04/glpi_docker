# GLPI on Docker

_based on [Diouxx](https://github.com/DiouxX/docker-glpi) docker image and [docker compose example](https://github.com/DiouxX/docker-glpi)_

## Prerequisite

- Docker

## Commands

### Run GLPI and MariaDB

`$ docker compose up -d`

### Stop GLPI and MariaDB

`$ docker compose down`

### Connect to mariadb shell

`$ docker exec -it mariadb bash`

### Dumb MariaDB database

`$ docker exec mariadb mysqldump --user root --password=diouxx glpidb > mysql_dump.sql `

## Setup

1. Using any browser, access to your local GLPI server with the address [glpi.localhost](glpi.localhost).
2. Select *Install*
3. Configure the database
   1. SQL's server name is *mariadb*
   2. SQL user is defined by the `MARIADB_USER` variable in the `mariadb.env` file
   3. SQL password is defined by the `MARIADB_PASSWORD` variable in the  `mariadb.env` file
4. Select the database named by the variable `MARIADB_DATABASE` defined in the `mariadb.env` file

## Connection to your GLPI server

By default, 4 accounts are created:

|Username|Password|Account type|
|---|---|---|
|glpi|glpi|Admin|
|tech|tech|Technician|
|normal|normal|Normal|
|post-only|postonly| Post only|
