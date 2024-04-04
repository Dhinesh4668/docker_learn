# 100 days of Docker learn 

### day 7, 

## Today we learn about , ``Docker`` container manage, 

### Today we see about docker contaner managing

## Table of Contents

- [Viewing Docker Containers](#into)
- [Starting and Stopping Containers](#start/stop)
- [Inspecting Containers](#inspet)
- [Removing Containers](#remove)
- [Managing Container Resources](#manage)
- [Conclution](#conclusion)


# Viewing Docker Containers

To view information about Docker containers, you can use the docker ps command. This command lists running containers by default.

```bash
docker ps
```

To view all containers, including stopped ones, use the -a flag:

```bash
docker ps -a
```

# Starting and Stopping Containers

## Starting Containers

To start a stopped container, use the docker start command followed by the container ID or name:

```bash
docker start <container_id_or_name>
```

## Stopping Containers

To stop a running container, use the docker stop command followed by the container ID or name:

```bash
docker inspect <container_id_or_name>
```

- This command provides a JSON-formatted output containing various details about the container, such as its configuration, networking, and resource usage.

##  Removing Containers

To remove a container, use the docker rm command followed by the container ID or name:

```bash
docker rm <container_id_or_name>
```
You can also remove multiple containers at once by ``specifying their IDs`` or ``names`` separated by spaces.


## Managing Container Resources

### Resource Limits

Docker allows you to set resource limits on containers, such as CPU and memory limits, to ensure fair resource allocation and prevent one container from monopolizing resources.

```bash
docker run --cpu-quota=50000 --memory=512m my_container
```

# Container Logs

You can view the logs of a container using the docker logs command followed by the container ID or name:

```bash 
docker logs <container_id_or_name>
```

# Conclusion
Congratulations on completing Day 7 of learning Docker! You now have a solid understanding of managing Docker containers efficiently. Experiment with the commands and techniques discussed in this guide to gain practical experience with Docker container management.

In the next lesson, we'll explore Docker networking and how to connect containers together to build more complex applications.


# resource

- [youtube](https://www.youtube.com/watch?v=3c-iBn73dDE&pp=ygUGZG9ja2Vy)

- [Official Doc](https://docs.docker.com/manuals/)