## To run jenkins as a container

```
$ docker run --name jenkins-master -p 8080:8080 -p 50000:50000 -d jenkins/jenkins:lts
```

## To run jenkins with docker volume

```
$ docker volume create jenkins_home
$ docker run --name jenkins-master -p 8080:8080 -p 50000:50000 -v jenkins_home:/var/jenkins_home -d jenkins/jenkins:lts
```

##### Reference:

[Jenkins Docker Hub](https://hub.docker.com/r/jenkins/jenkins/)
