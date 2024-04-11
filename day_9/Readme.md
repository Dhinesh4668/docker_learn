# Day 09

## Content

- [Writing a Dockerfile](#writing-a-dockerfile)
- [Building Docker Image](#building-docker-image)
- [Running Docker Container](#running-docker-container)
- [Basic Docker Operations](#basic-docker-operations)
- [Docker Compose (Optional)](#docker-compose-optional)

---

## Writing a Dockerfile

A Dockerfile is a text document that contains all the commands a user could call on the command line to assemble an image. It provides a clear and concise way to automate the creation of Docker images.

### Basic Explanation:

- `FROM`: Specifies the base image to use for the container. In this case, we're using the latest version of Ubuntu.
- `WORKDIR`: Sets the working directory for subsequent instructions in the Dockerfile.
- `COPY`: Copies files and directories from the host into the container's filesystem at a specified location.
- `RUN`: Executes commands inside the container during the build process. Here, we're updating the package list and installing required dependencies.
- `ENV`: Sets environment variables within the container.
- `CMD`: Specifies the default command to run when the container starts. In this case, it runs a JavaScript named index.js.

Create a file named `Dockerfile` in your project directory. This file contains instructions to build your Docker image.

```Dockerfile
# Use an official base image
FROM ubuntu:latest

# Set the working directory in the container
WORKDIR /app

# Copy the current directory contents into the container at /app
COPY . /app

# Install any needed dependencies
RUN apt-get update && apt-get install -y \
    <your_dependency_packages>

# Define environment variable
ENV NAME World

# Run node when the container launches
CMD ["node", "index.js"]
```

# Building Docker Image:

After writing the Dockerfile, users are instructed to open a terminal in their project directory and run the docker build command to build the Docker image.

Explanation: <br>
``docker build:`` Builds a Docker image from a Dockerfile and a context (the specified directory). The -t flag is used to tag the image with a name (here, my_image), and specifies the build context (current directory).

```bash
docker build -t my_image .
```

# Running Docker Container
Once the Docker image is built, users can run a container based on this image using the docker run command.

Explanation:<br>
``docker run:`` Runs a Docker container from a specified image. The -it flags allocate a pseudo-TTY and keep STDIN open even if not attached, allowing interaction with the container. <br>``--name`` specifies a name for the container, and ``my_image`` refers to the previously built Docker image.


```docker
docker run -it --name my_container my_image
```

[example code 👉🚀](./ex/Dockerfile)