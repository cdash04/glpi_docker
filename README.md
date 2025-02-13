# GLPI on Docker

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
