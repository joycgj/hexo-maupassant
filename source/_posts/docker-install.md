---
title: Install Docker and run hello-world
date: 2017-02-16 15:10:50
category: virtualization
tags: docker,virtualization
toc: true
---


# What is Docker

Docker is the world's leading software containerization platform.
[https://docs.docker.com](https://docs.docker.com)

# Install Docker for Mac

If you have not yet installed Docker for Mac, please see [Install Docker for Mac](https://docs.docker.com/docker-for-mac/install/) for an explanation of stable and beta channels, download and install information.

# Get started with Docker for Mac

Docker is a full development platform for creating containerized apps, and Docker for Mac is the best way to get started with Docker on a Mac. [Get started with Docker for Mac](https://docs.docker.com/docker-for-mac/)

## Check versions of Docker Engine, Compose, and Machine

Run these commands to test if your versions of docker, docker-compose, and docker-machine are up-to-date and compatible with Docker.app.

```
$ docker --version
Docker version 1.13.1, build 092cba3

$ docker-compose --version
docker-compose version 1.11.1, build 7c5d5e4

$ docker-machine --version
docker-machine version 0.9.0, build 15fd4c7
```

## Explore the application and run examples

1. Open a command-line terminal, and run some Docker commands to verify that Docker is working as expected.
Some good commands to try are docker version to check that you have the latest release installed, and docker ps and docker run hello-world to verify that Docker is running.

2. For something more adventurous, start a Dockerized web server.

```
docker run -d -p 80:80 --name webserver nginx
```

If the image is not found locally, Docker will pull it from Docker Hub.
In a web browser, go to http://localhost/ to bring up the home page. (Since you specified the default HTTP port, it isn’t necessary to append :80 at the end of the URL.)

![Welcome to nginx](https://docs.docker.com/docker-for-mac/images/hello-world-nginx.png)

3. Run **docker ps** while your web server is running to see details on the webserver container.

4. Stop or remove containers and images.
The nginx webserver will continue to run in the container on that port until you stop and/or remove the container. If you want to stop the webserver, type: docker stop webserver and start it again with docker start webserver. A stopped container will not show up with docker ps; for that, you need to run docker ps -a.
To stop and remove the running container with a single command, type: docker rm -f webserver. This will remove the container, but not the nginx image. You can list local images with docker images. You might want to keep some images around so that you don’t have to pull them again from Docker Hub. To remove an image you no longer need, use docker rmi followed by an image ID or image name. For example, docker rmi nginx.





