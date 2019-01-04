## To run nginx as a docker container

```
$ docker run --name nginx -d -p 8080:80 nginx
```

### For debugging purposes

```
$ docker logs nginx

$ docker exec -it nginx sh
```
