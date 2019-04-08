# copy instruction

- Create a dummy file

```
vi login.html 
```

- Create a Dockerfile

```
FROM busybox
copy login.html .
CMD sleep 1000
```

- Build the docker image

```
$ docker build -t copy-image .
```

- Deploy the image as a container

```
$ docker run -d --name copy-container copy-image 
```
