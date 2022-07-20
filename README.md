# learn-docker

# Docker

## Container

#### Create and Run container
```
docker run --rm --name test-redis -v redis:/data:rw redis:alpine --loglevel debug
```
`--rm`: run and remove container<br>
`--name <container_name>`<br>
`-v <host_dir>:<container_dir>:<[option]>`: persist container data to host_dir<br>
`<remote_container:tag>`

#### Show running containers
```
docker ps
```

#### Remove running container
```
docker rm -f <...container_id>
```

## Image

#### Show local images
```
docker image ls
```

#### Push / Pull container
```
docker push/pull <remote_container:tag>
```

## Volume

#### Create volume
```
docker volume create -o <options> <volume_name>
```

#### Show volumes
```
docker volume ls
```

#### Inspect volume
```
docker volume inspect <volume_name>
```

#### Delete volumes
```
docker volume rm -f <...volume_name>
```

## Use container
```
docker exec -it <container_name> <command>
```
`<container_name>`: running container_name name
`<command>`: `redis-cli`, other linux commands

## Docker Compose

