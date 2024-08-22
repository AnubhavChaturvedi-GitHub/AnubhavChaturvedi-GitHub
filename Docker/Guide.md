# Docker Guide

## Introduction

Docker is a tool designed to make it easier to create, deploy, and run applications by using containers. Containers allow developers to package up an application with all parts it needs, such as libraries and other dependencies, and ship it all out as one package.

## Prerequisites

- **Basic Knowledge:** You should be familiar with basic terminal commands.
- **Tools:** Docker should be installed on your system. [Install Docker](https://docs.docker.com/get-docker/).

## Table of Contents

1. [Docker Basics](#docker-basics)
2. [Setting Up Docker](#setting-up-docker)
3. [Creating Your First Container](#creating-your-first-container)
4. [Docker Images](#docker-images)
5. [Dockerfile](#dockerfile)
6. [Docker Compose](#docker-compose)
7. [Managing Containers](#managing-containers)
8. [Best Practices](#best-practices)
9. [Resources](#resources)

## Docker Basics

### What is Docker?
- **Containers:** Lightweight, standalone, and executable packages that include everything needed to run a piece of software.
- **Images:** Immutable templates that define the contents of a container.

### Key Commands
- `docker`: Main command-line interface for Docker.
- `docker run`: Run a command in a new container.
- `docker build`: Build an image from a Dockerfile.
- `docker pull`: Download an image from a registry.
- `docker push`: Upload an image to a registry.

## Setting Up Docker

1. **Installation:**
   - **Linux:** Follow [this guide](https://docs.docker.com/engine/install/ubuntu/).
   - **Windows/Mac:** Download Docker Desktop from [here](https://docs.docker.com/get-docker/).

2. **Verify Installation:**
   ```bash
   docker --version
   ```

3. **Start Docker:**
   - Docker Desktop should start automatically. On Linux, use:
     ```bash
     sudo systemctl start docker
     ```

## Creating Your First Container

1. **Run a Simple Container:**
   ```bash
   docker run hello-world
   ```
   - This command pulls the `hello-world` image from Docker Hub and runs it in a container.

2. **Interactive Containers:**
   ```bash
   docker run -it ubuntu
   ```
   - `-it` flag lets you interact with the container.

3. **List Running Containers:**
   ```bash
   docker ps
   ```

4. **Stop a Container:**
   ```bash
   docker stop <container_id>
   ```

## Docker Images

1. **Search for Images:**
   ```bash
   docker search nginx
   ```

2. **Pull an Image:**
   ```bash
   docker pull nginx
   ```

3. **Run an Image:**
   ```bash
   docker run -d -p 80:80 nginx
   ```
   - `-d`: Detached mode, runs the container in the background.
   - `-p`: Maps container's port 80 to host's port 80.

4. **List Images:**
   ```bash
   docker images
   ```

5. **Remove an Image:**
   ```bash
   docker rmi <image_id>
   ```

## Dockerfile

1. **What is a Dockerfile?**
   - A `Dockerfile` is a text document that contains all the commands to assemble an image.

2. **Creating a Simple Dockerfile:**
   ```Dockerfile
   # Use an official Python runtime as a parent image
   FROM python:3.8-slim

   # Set the working directory in the container
   WORKDIR /app

   # Copy the current directory contents into the container
   COPY . /app

   # Install any needed packages specified in requirements.txt
   RUN pip install --no-cache-dir -r requirements.txt

   # Make port 80 available to the world outside this container
   EXPOSE 80

   # Run app.py when the container launches
   CMD ["python", "app.py"]
   ```

3. **Build an Image:**
   ```bash
   docker build -t my-python-app .
   ```

4. **Run Your Image:**
   ```bash
   docker run -p 4000:80 my-python-app
   ```

## Docker Compose

1. **What is Docker Compose?**
   - A tool for defining and running multi-container Docker applications.

2. **Creating `docker-compose.yml`:**
   ```yaml
   version: '3'
   services:
     web:
       image: nginx
       ports:
         - "80:80"
     redis:
       image: "redis:alpine"
   ```

3. **Running Docker Compose:**
   ```bash
   docker-compose up
   ```

4. **Stopping Docker Compose:**
   ```bash
   docker-compose down
   ```

## Managing Containers

1. **List All Containers:**
   ```bash
   docker ps -a
   ```

2. **Starting a Container:**
   ```bash
   docker start <container_id>
   ```

3. **Stopping a Container:**
   ```bash
   docker stop <container_id>
   ```

4. **Remove a Container:**
   ```bash
   docker rm <container_id>
   ```

## Best Practices

1. **Use Official Images:** Always start with official images from Docker Hub.
2. **Keep Dockerfiles Simple:** Avoid adding unnecessary layers.
3. **Security:** Don’t run containers as root.
4. **Multi-Stage Builds:** Use multi-stage builds to optimize the size of your images.

## Resources

- [Docker Documentation](https://docs.docker.com/)
- [Docker Hub](https://hub.docker.com/)
- [Dockerfile Best Practices](https://docs.docker.com/develop/develop-images/dockerfile_best-practices/)
