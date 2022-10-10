# Docker-cheatsheet
Some commands to deal with docker containers in daily usage.
Ensure to be part of the docker group, otherwise you need root permission to run most of these commands.

### Create a container with R v4.0.4 and bash
It is advisable to specify the tag, so the version rather than just using "latest".
Sharing a volume with the host is common. It is performed with -v indacating first host volume path then the container one.
```
docker run -ti -v "$PWD":/home/docker r-base:4.0.4 bash
```

### View containers list
```
docker ps -a
```

### View active containers
```
docker ps     
```

### Run a command on already running container
```
docker exec -it <containerID> <command>
```

### Run a already created container (if stopped)
```
docker start -i <containerID>
```

### Remove a container keeping the image
```
docker rm <containerID>
```

### Remove an image
```
docker image rm <imageID>
```

### Remove a repository with same name and image id but different tag
```
docker rmi <repository_name>:<tag>
```


## TODO
	- Dockerfile
