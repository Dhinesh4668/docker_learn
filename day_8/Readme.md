
#### Dcoker componse 

* What is ``DOCKER COMPOSE``: 

    Docker Compose is a tool for defining and running multi-container Docker applications. It allows you to define your application’s services, networks, and volumes in a single file, making it easier to manage and deploy complex applications. 

### Using Docker Compose for ``Multi-Container`` Applications:

step 1

* Docker compose Install:
        Ensure Docker Compose is installed on your system. Follow the official documentation
[Documentation](https://docs.docker.com/compose/install/)

* Creating a Docker Compose file :

    creating  a file named as ``docker-compose.yml``, in your project workspace 

    ```yml
    <!-- docker-compose.yml -->
        version: '3'
        services:
        web:
            build: .
            ports:
            - "3000:3000"
        redis:
            image: "redis:alpine"
    ```

* Define your Application service

    * in example , we define a two service:
        
        * ``web``: Represents our Node.js application, built using the Dockerfile in the current directory and exposed on port 3000.
        * ``redis``: Uses the official Redis image from Docker Hub. 

    