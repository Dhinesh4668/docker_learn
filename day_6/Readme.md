# 100 days of docker learn is day 5 & 6
## in this session , we will see about in-depth knowlage of dockerfile , and docker images


##### day 5  previous recap 

* whats is **docker** : docker is the containerized application development , we can create the application rapidly in isolated platforms

* what is **docker** **container** : ``docker container``  is a lightweight, standalone, executable software package that includes everything needed to run a piece of software, including the code, runtime, system tools, system libraries, and settings. Docker containers are based on Docker technology, which allows applications to be packaged into containers and then run consistently across different environments, such as development, testing, and production.

* ``docker commands`` 

    1. docker version check 

        * ```bash
            #check the docker version
            docker --version
            ``` 
    2. ``docker info``: display the docker system -wide information

        * ```bash 
            #docker info
            docker info 
            #its shows the docker sys wide information
            ```

    3. ``docker search``: docker search , to search the repository / rigistry from docker hub 

        * ```bash
            #docker search <image>
            docker search ubuntu 
            ```
    4. ``docker pull`` : docker pull an image or repo from the regestory.

        * ```bash
            docker pull [option] NAME:[TAG] 
            ```

    5. ``docker images``: list the available images.

        * ```bash
            #docker list the images
            docker images [options] [repository:tag] 
            ```

    6. ``docker ps``: docker ps is listing the available runing images docker local hub

        * ```bash
            docker ps 
            ```

    7. ``docker run`` : create and start a new container based on a docker image.

        * ```bash
            docker run [option] image [command] [arg...] 
            ```

    8. ``docker exec``: run a command in a runing container 
        
        * ```bash
            docker exec [option] container command [arg....]
            ```

    9. ``docker stop``: docker stop command is a to stop one / more running containers 

        * ```bash
            docker stop [option] container [container..]
            ``` 

    10. ``docker rm``: docker rm is a remove one or more container 

        * ```bash
            docker rm [option] container [container..]
            ```

    11. ``docker prune``: docker prun is to remove/ deleting the running and non running container .

        * ```bash
            docker prune [option] conatiner [container.....] 
            ```

##### thise are the some basic docker operations commands 

explore more means [!]
=======
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
>>>>>>> 2f9f6efe81264fce5b8bc9a6fc8e2180711ba9cf
