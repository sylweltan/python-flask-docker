# python-flask-docker
Basic Python Flask app in Docker which prints the hostname and IP of the container

## Here it is - the hero of our evening. Please welcome "THE BADGE" for MAIN.YML:
![CI](https://github.com/sylweltan/python-flask-docker/workflows/CI/badge.svg)


## welcome also our next friend - the dockerimage.yml 
![My Application](https://github.com/sylweltan/python-flask-docker/workflows/My%20Application/badge.svg)


### Build application
Build the Docker image manually by cloning the Git repo.
```
$ git clone https://github.com/lvthillo/python-flask-docker.git
$ docker build -t lvthillo/python-flask-docker .
```

### Download precreated image
You can also just download the existing image from [DockerHub](https://hub.docker.com/r/lvthillo/python-flask-docker/).
```
docker pull lvthillo/python-flask-docker
```

### Run the container
Create a container from the image.
```
$ docker run --name my-container -d -p 8080:8080 lvthillo/python-flask-docker
```

Now visit http://localhost:8080
```
 The hostname of the container is 6095273a4e9b and its IP is 172.17.0.2. 
```

### Verify the running container
Verify by checking the container ip and hostname (ID):
```
$ docker inspect -f '{{range .NetworkSettings.Networks}}{{.IPAddress}}{{end}}' my-container
172.17.0.2
$ docker inspect -f '{{ .Config.Hostname }}' my-container
6095273a4e9b
```

### Tera kurna my
oh, really ?
