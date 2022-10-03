# flaskMariaDocker
## Practising Flask App with MariaDB as Database inside Docker Container

##### Commands For MariaDB

```
$ docker pull mariadb:10.9.3

$ docker run --name mariadb_practice -e MYSQL_ROOT_PASSWORD=lxIsLazy -p 3308:3308 -d docker.io/library/mariadb:10.9.3

$ docker ps

$ docker stop mariadb_practice

$ docker restart mariadb_practice

$ docker exec -it mariadb_practice bash

$ docker inspect -f '{{range .NetworkSettings.Networks}}{{.IPAddress}}{{end}}' mariadb_practice
```

##### Other Ways to do something

```
$ docker run --detach --name mariadb_pract --env MARIADB_USER=lx --env MARIADB_PASSWORD=lxIsPassword --env MARIADB_ROOT_PASSWORD=lxIsRoot mariadb:10.9.3
```
- **mariadb_pract** is the name you want to assign to your container, 
- **lxIsRoot** is the password to be set for the MariaDB root user

```
$ docker network create network_lx 
$ docker run --detach --network network_lx --name mariadb_pract --env MARIADB_USER=lx --env MARIADB_PASSWORD=lxIsPassword --env MARIADB_ROOT_PASSWORD=lxIsRoot mariadb:10.9.3
```

:: ref - (Docker Hub)[https://hub.docker.com/_/mariadb]