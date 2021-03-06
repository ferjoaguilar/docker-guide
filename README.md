<p align="center">
    <img alt="Curso de Next.js" src="https://www.docker.com/wp-content/uploads/2022/03/horizontal-logo-monochromatic-white.png.webp" width="120" />
</p>
<h1 align="center">
  Docker Guide
</h1>
<p align="center">
  Written by Fernando Jose Aguilar Rivas
</p>

# General
This is a complete guide about docker commands, functions and others. using docker guia to create container, volumnes and networks, personally docker guide is written to use with NodeJS and Golang but is created with general purpose.

## Table of content

## General commands

docker utilities

| Command | Param | Agregate | Description | Example |
| ------------ | ------------ | ------------ | ------------ | ------------ |
|  docker inspect | - |  container ID | Inspect container information | docker inspect 7e5b48afe796 |
|  docker rename | - |  container name | Change name to container | docker rename origialname newname |
|  docker rm | - |  container ID | Remove container to ps | docker rm 7e5b48afe796 |
|  docker container prune | - |  container ID | Remove all to stop container | docker container prune |
|  docker stop | - |  container ID | Stop container | docker stop 7e5b48afe796 |
|  docker logs | - |  container ID | Show container logs | docker logs proxy |
|  docker logs | -f |  container ID | Show container logs in realtime | docker logs -f proxy |
|  docker logs | --tail |  container ID | Show container logs from ultimate lines | docker logs --tail 10 -f proxy |


**Command:** docker run

| Command | Param | Agregate | Description | Example |
| ------------ | ------------ | ------------ | ------------ | ------------ |
|  docker run | -  |  image name | Execute a container | docker run hello-world |
|  docker run | --name  |  container name | Execute a container with name | docker run --name hello-platzi hello-world |
|  docker run | -it | image name | Execute a container in interactive mode | docker run -it ubuntu |
|  docker run | -d, --detach | image name | Execute a container to background | docker run -d ubuntu tail -f /dev/null|
|  docker exec | - | container name | Entry to container running | docker exec -it ubuntu bash|
|  docker run | -p, --publish | localport:containerport | Listen port | docker run -d --name proxy --publish 8080:80 nginx |

**Command:** docker ps

| Command | Param | Agregate | Description | Example |
| ------------ | ------------ | ------------ | ------------ | ------------ |
|  docker ps | -  | - | Show running containers  | docker ps |
|  docker ps | -a, --all | - | Show all containers (dead or live) | docker ps -a |


## Bind mounts

Share information in local folder to docker container.

| Command | Param | Agregate | Description | Example |
| ------------ | ------------ | ------------ | ------------ | ------------ |
|  docker run | -v  | localpath:containerpath | Share information local folder to docker container  | docker run -d --name mongodb -v /home/feraguilar/Escritorio/docker-data:/data/db mongo |

## Volumes

Space reserved only for docker. It's a security space management to docker containers.

| Command | Param | Agregate | Description | Example |
| ------------ | ------------ | ------------ | ------------ | ------------ |
|  docker volume | ls  | - | Show all docker volumes  | docker volume ls |
|  docker volume | create  | volume name | Create new volume  | docker volume create mongodata |
|  docker run | --mount  | src=volume,dst=containerdata | Assign volume to container  | docker run -d --name mongodb --mount src=mongodata,dst=/data/db mongo |
|  docker volume | rm | volume name | Remove volume | docker volume rm mongodata |

## Images

| Command | Param | Agregate | Description | Example |
| ------------ | ------------ | ------------ | ------------ | ------------ |
|  docker image | ls  | - | Show all docker images  | docker image ls |
|  docker pull | -  | image name | Download docker image  | docker pull ubuntu |
|  docker image | rm  | image name | Remove docker image  | docker image rm ubuntu |
|  docker history | -  | - | Show tracking docker image  | docker history ubuntu |

## Dockerfile

Dockerfile allow to build custom images

### Docker build

| Command | Param | Agregate | Description | Example |
| ------------ | ------------ | ------------ | ------------ | ------------ |
|  docker build | -t, --tag  | image name | Build custom image  | docker build -t ubuntu:platzi . |


<p align="center">
    <img alt="Created by Fernando Aguilar" src="https://res.cloudinary.com/dohkdu219/image/upload/v1642443309/portfolio/signature_oq60qf.png" width="80%" />
</p>



