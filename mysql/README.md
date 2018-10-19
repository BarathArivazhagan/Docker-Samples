# MYSQL service as a container

## MYSQL service

```
$ docker run --name mysql-db  -e MYSQL_ROOT_PASSWORD=root  -d mysql:latest
```

## MYSQL service with mounted volume

```
docker run --name mysql-db  -v /Users/barath/mysql_data/:/var/lib/mysql -e MYSQL_ROOT_PASSWORD=root  -d mysql:latest
```
