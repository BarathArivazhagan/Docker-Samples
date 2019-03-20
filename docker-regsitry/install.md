# Steps to run docker registry as a container


## Generate basic auth htpasswd
```

# set up basic authentication
$ mkdir auth
$ docker run --rm --entrypoint htpasswd registry:2 -Bbn testuser testpassword > auth/nginx.htpasswd


# start docker registry

$ docker run -d -p 5000:5000 -p 8080:80 --restart=always --name registry -v "$(pwd)"/auth:/auth -e "REGISTRY_AUTH=htpasswd" -e "REGISTRY_AUTH_HTPASSWD_REALM=Registry Realm" -e REGISTRY_AUTH_HTPASSWD_PATH=/auth/htpasswd registry:2
```

