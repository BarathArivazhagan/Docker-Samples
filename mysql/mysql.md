# MYSQL service as a container

#### MYSQL service

```
$ docker run --name mysql-db -p 3306:3306 -e MYSQL_ROOT_PASSWORD=root  -d mysql:latest
```

#### MYSQL service with mounted volume

```
$ docker run --name mysql-db  -p 3306:3306 -v /Users/barath/mysql_data/:/var/lib/mysql -e MYSQL_ROOT_PASSWORD=root  -d mysql:latest
```


#### MYSQL service with docker volume

```
$ docker volume create mysql-data
$ docker run --name mysql-db  -p 3306:3306 -v mysql-data/:/var/lib/mysql -e MYSQL_ROOT_PASSWORD=root  -d mysql:latest
```
