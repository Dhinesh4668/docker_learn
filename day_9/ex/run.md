- To build and run this Dockerized Node.js application:

- ``Save the index.js`` and ``Dockerfile`` in the same directory.
- ``Open a terminal`` in the directory containing these files.
- Run the following command to build the Docker image:

```docker
docker build -t my_node_app .
```
- After the image is built, you can run a container based on this image:

```docker
docker run -d --name my_node_container -p 3000:3000 my_node_app
```

* This will start a container named ``my_node_container `` based on the ``my_node_app image``, exposing ``port 3000`` on the host. You can access the Node.js application by navigating to`` http://localhost:3000 ``in your web browse