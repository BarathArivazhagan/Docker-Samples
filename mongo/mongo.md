# MongoDB as a container

## MongoDB
```
$ docker run -d --name mongo mongo:latest
```

## MongoDB with Authentication

```
$ docker run -d --name mongo -e MONGO_INITDB_ROOT_USERNAME=root -e MONGO_INITDB_ROOT_PASSWORD=root mongo:latest
```
