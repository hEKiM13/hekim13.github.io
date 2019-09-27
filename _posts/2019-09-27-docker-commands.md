---
published: true
author: Michael
title:  "Docker commands"
categories: [docker]
tags: [docker]
---

Below are the Docker commands I use most frequently and sometimes forget.

# Docker commands

## Build

| Command | Description |
| ------- | ----------- |
| `docker build -t <image-name>:<tag> .` | Build, name and tag a Docker image and supply the current directory as the build context |

## Run

| Command | Description |
| ------- | ----------- |
| `docker run -d --rm -p <host-port>:<container-port> --name <container-name> <image-name>` | Run a detached `-d` container of the image `<image-name>` and name it `<container-name>`. Expose ports `-p` and remove `--rm` it when the main process ends |
| `docker exec -it <container-name> bash` | Connect to a `bash` instance in the running container `<container-name>` |

## Image management

| Command | Description |
| ------- | ----------- |
| `docker image prune` | Remove all unused Docker images |
| `docker rmi <image-sha>` | Remove the Docker image with the `<image-sha>` |
