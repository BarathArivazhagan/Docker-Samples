###  To run rabbitmq service as docker container

```
docker run -d  --name rabbitmq-service -p 5672:5672 -p 15672:15672 -e RABBITMQ_DEFAULT_USER=rabbituser -e RABBITMQ_DEFAULT_PASS=rabbitpassword rabbitmq:3-management
```
