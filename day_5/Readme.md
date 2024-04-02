# 100 days of docker learn is day 5
## in this session , we will see about in-depth knowlage of dockerfile , and docker images


##### day 5  previous recap 

* whats is **docker** : docker is the containerized application development , we can create the application rapidly in isolated platforms

* what is **docker** **container** : ``docker container``  is a lightweight, standalone, executable software package that includes everything needed to run a piece of software, including the code, runtime, system tools, system libraries, and settings. Docker containers are based on Docker technology, which allows applications to be packaged into containers and then run consistently across different environments, such as development, testing, and production.


# Docker Installation Guide

## Windows

1. **Download Docker Desktop for Windows**: 
   - Visit the [Docker Hub](https://hub.docker.com/editions/community/docker-ce-desktop-windows) page.
   - Click on "Get Docker Desktop for Windows".
   - Follow the instructions in the installer to complete the installation.

2. **Enable Virtualization**: 
   - Make sure virtualization is enabled in your BIOS settings. Docker Desktop requires virtualization to run containers.

3. **Start Docker Desktop**: 
   - Once installed, Docker Desktop should start automatically.
   - You'll see the Docker icon in the system tray when it's running.

4. **Verify Installation**: 
   - Open a command prompt and run `docker --version` to verify that Docker is installed correctly.
   - Run `docker run hello-world` to verify that Docker can pull and run containers.

## Linux

1. **Update Package Index**: 
   - Update the apt package index:
     ```
     sudo apt-get update
     ```

2. **Install Docker Dependencies**: 
   - Install packages to allow apt to use a repository over HTTPS:
     ```
     sudo apt-get install \
        apt-transport-https \
        ca-certificates \
        curl \
        software-properties-common
     ```

3. **Add Docker's Official GPG Key**: 
   - Add Docker’s official GPG key:
     ```
     curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
     ```

4. **Set up Docker Repository**: 
   - Set up the stable repository:
     ```
     sudo add-apt-repository \
        "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
        $(lsb_release -cs) \
        stable"
     ```

5. **Install Docker CE**: 
   - Update the apt package index again and install Docker CE:
     ```
     sudo apt-get update
     sudo apt-get install docker-ce
     ```

6. **Start Docker**: 
   - Docker should now be installed and running.
     ```
     sudo systemctl start docker
     ```

7. **Verify Installation**: 
   - Check that it's installed correctly by running the hello-world image:
     ```
     sudo docker run hello-world
     ```

## macOS

1. **Download Docker Desktop for Mac**: 
   - Visit the [Docker Hub](https://hub.docker.com/editions/community/docker-ce-desktop-mac) page.
   - Click on "Get Docker Desktop for Mac".
   - Follow the instructions in the installer to complete the installation.

2. **Start Docker Desktop**: 
   - Once installed, Docker Desktop should start automatically.
   - You'll see the Docker icon in the menu bar when it's running.

3. **Verify Installation**: 
   - Open a terminal and run `docker --version` to verify that Docker is installed correctly.
   - Run `docker run hello-world` to verify that Docker can pull and run containers.


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


    12. ``docker run Command:``
The docker run command is used to create and start containers based on Docker images. Here are some common options:

    * ``-d, --detach:`` Run container in the background.
    
    * ``-it, --interactive:`` Keep STDIN open even if not attached, allocate a pseudo-TTY.
    
    * ``-p, --publish:`` Publish a container's port(s) to the host.
    
    * ``-v, --volume:`` Bind mount a volume.

    * ``--name:`` Assign a name to the container.
    
    * ``--rm:`` Automatically remove the container when it exits.
    
    * ``--env:`` Set environment variables.
    
    * ``--network:`` Connect a container to a network.

``Example:``

```bash 
    docker run -d -p 8080:80 nginx
```

This command creates and starts a new container based on the nginx image, runs it in detached mode (-d), and publishes port 80 of the container to port 8080 on the host.

Remember, these are just a few examples of Docker commands. There are many more options and variations available for each command. You can explore more by using docker --help or docker COMMAND --help.

##### thise are the some basic docker operations commands 

* explore more means dokcer commands [! preview](../day_4/Dockerfile)

* document refercence [! previrw](https://docs.docker.com/)

# youtube refercene

1. [![YouTube Preview](https://img.youtube.com/)](https://www.youtube.com/watch?v=3c-iBn73dDE&pp=ygUHZG9ja2VyIA%3D%3D)
