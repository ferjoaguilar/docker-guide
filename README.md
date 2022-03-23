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

**Command:** docker run

| Command | Param | Agregate | Description | Example |
| ------------ | ------------ | ------------ | ------------ | ------------ |
|  docker run | -  |  image name | Execute a container | docker run hello-world |
|  docker run | --name  |  container name | Execute a container with name | docker run --name hello-platzi hello-world |

**Command:** docker ps

| Command | Param | Agregate | Description | Example |
| ------------ | ------------ | ------------ | ------------ | ------------ |
|  docker ps | -  | - | Show running containers  | docker ps |
|  docker ps | -a, --all | - | Show all containers (dead or live) | docker ps -a |
