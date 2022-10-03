# flaskMariaDocker

## Practising Flask App with MariaDB as Database inside Docker Container

##### Commands Performed For MariaDB

```
$ docker pull mariadb:10.9.3

$ docker run --name mariadb_practice -e MYSQL_ROOT_PASSWORD=lxIsLazy -p 3308:3308 -d docker.io/library/mariadb:10.9.3

$ docker ps

$ docker stop mariadb_practice

$ docker restart mariadb_practice

$ docker exec -it mariadb_practice bash

$ docker inspect -f '{{range .NetworkSettings.Networks}}{{.IPAddress}}{{end}}' mariadb_practice
```
