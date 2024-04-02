# Day 6: Exploring Docker Commands and Workflow

Welcome to Day 6 of our Docker learning journey! Today, we're diving into some essential Docker commands and exploring practical use cases to solidify our understanding.

## Basic Docker Commands

Let's start by revisiting some basic Docker commands:

### Docker Login

To authenticate to a Docker registry, we use the `docker login` command. Before pushing images to Docker Hub, we need to log in:

```bash
docker login
```

## Pulling Ubuntu Image

We can pull the Ubuntu image from Docker Hub using the docker pull command:

```bash 
docker pull ubuntu
```

## Working with Image and OS Files

To work with an image's file system and the OS within a container, we can start an interactive shell in an Ubuntu container:

```bash 
docker run -it ubuntu /bin/bash
```

### Pulling and Running Nginx

Let's pull the Nginx image and run a sample Node.js application:

```bash 
docker pull nginx
docker run -d -p 8080:80 nginx
```

## Port Mapping
Port mapping allows us to map container ports to host ports using the ``-p`` flag:

```bash
docker run -d -p HOST_PORT:CONTAINER_PORT IMAGE_NAME
```

## Copying Files
We can copy files from the host to a Docker container using docker cp:

```bash
docker cp HOST_PATH CONTAINER_ID:CONTAINER_PATH
```

## Exporting Docker Container
To export a Docker container to a tar archive, we use the docker export command:

```bash
docker export CONTAINER_ID > container.tar
```

## Publishing Image to Docker Hub
Finally, let's tag our Docker image and push it to Docker Hub for sharing:

```bash 
docker tag IMAGE_NAME USERNAME/REPOSITORY:TAG
docker push USERNAME/REPOSITORY:TAG
```


## Running Node.js Server with Nginx
To demonstrate running a Node.js server using Nginx as a reverse proxy, here's an example Node.js server code:

```js
const http = require('http');

const PORT = process.env.PORT || 3000;

const server = http.createServer((req, res) => {
  res.writeHead(200, {'Content-Type': 'text/plain'});
  res.end('Hello from Node.js server!\n');
});

server.listen(PORT, () => {
  console.log(`Server running at http://localhost:${PORT}/`);
});
```
# example [example](./ex/Readme.md)

## Workflow
1. Login to Docker Hub: Before pushing our image, we need to log in to Docker Hub using docker login.

2. Pull Ubuntu Image: Pull the Ubuntu image from Docker Hub to use it as a base image for our experiments.

3. Work with Image and OS Files: Enter an interactive shell in the Ubuntu container to explore its file system and perform tasks.

4. Pull and Run Nginx: Pull the Nginx image and run a sample Node.js application, mapping container port 80 to host port 8080.

5. Copy Files: Copy any necessary files from the host to the running Docker container using docker cp.

6. Export Docker Container: Export the Docker container to a tar archive for backup or sharing purposes.

7. Publish Image to Docker Hub: Tag your Docker image with your Docker Hub username and repository name, and then push it to Docker Hub for sharing with others.
