## To run jenkins as a container

```
$ docker run --name jenkins-master -p 8080:8080 -p 50000:50000 -d jenkins/jenkins:lts
```

## To run jenkins with docker volume

```
$ docker volume create jenkins_home
$ docker run --name jenkins-master -p 8080:8080 -p 50000:50000 -v jenkins_home:/var/jenkins_home -d jenkins/jenkins:lts
```

## Retrieve jenkins admin password from docker logs or docker exec

```
$ docker logs jenkins-master
```

## Attach docker socket to jenkins docker

```
$docker run -d --name jenkins -v /var/run/docker.sock:/var/run/docker.sock  -v jenkins_home:/var/jenkins_home -p 8080:8080 jenkins/jenkins:lts
```

##### Reference:

[Jenkins Docker Hub](https://hub.docker.com/r/jenkins/jenkins/)
