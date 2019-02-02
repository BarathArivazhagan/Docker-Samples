## To run nginx as a docker container

```
$ docker run --name nginx -d -p 8080:80 nginx
```

### For debugging purposes

```
$ docker logs nginx

$ docker exec -it nginx sh
```

### nginx with curl package

```
FROM nginx
RUN apt-get update && apt-get -y install curl
```
