# Launching an application in a Docker container

[Home](../../README.md) / [Docker](../README.md) / Launching an application

---

Frequently used commands

### Creating a shared network for containers

```shell
docker network create <network-name>
```

### Creating an image (Gradle)

```shell
docker build --build-arg JAR_FILE=build/libs/\*.jar -t <project>/<image-name> .
```

### Launching the container

```shell
docker run --network <network-name> --name <cntainer-name> -dp 8081:8081 <project>/<image-name>
```

### Displaying a list of containers

```shell
docker ps -a
```

### Connecting to the container shell

```shell
docker exec -it <cntainer-name> /bin/sh
```

### Real-time log output

```shell
docker logs -f <cntainer-name>
```

### Stopping and deleting a container

```shell
docker stop <cntainer-name> && docker rm <cntainer-name>
```

### Deleting an image

```shell
docker image rm <project>/<image-name>
```