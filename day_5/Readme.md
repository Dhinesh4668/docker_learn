# 100 days of docker learn is day 5
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