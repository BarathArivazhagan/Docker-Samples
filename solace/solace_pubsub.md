## To run solace PubSub standard as container

```
$ docker pull solace/solace-pubsub-standard

$ docker run -d -p 8080:8080 -p 55555:55555 --shm-size=2g --env username_admin_globalaccesslevel=admin --env username_admin_password=admin --name=solace solace/solace-pubsub-standard
```

### To access solace container

```
$ docker exec -it solace /usr/sw/loads/currentload/bin/cli -A
```

## Access solace dashboard 

http://localhost:8080
