# Add Volume to a running [Docker](https://www.docker.com/) Container

Same process goes for any external configuration changes that you might want to make once your container is up and running.

Step 0: List all the docker containers that are currently running on your machine using the following command.

```closure
docker ps
```

Output should look like a table. Note the container id that you want to add volume to.

Step 1: Commit the docker state to a local image.

```closure
docker commit <container-id> <local-image-name>
```

Step 2: Create a new container using the run command and add the volume that you want to add normally. Only difference is you should use the < local-image-name > that you used in previous step. To reinstate the configuration of the docker container.

```closure
docker run --detach -it -volume="$PWD/dir1":/dir1 --volume="$PWD/dir2":/dir2 --name <container-name> <local-image-name>
```

Step 3: Test your new container. In case of port conflicts you might need to shut down your old container.

After testing if you want the same name delete the old container and rename new container as needed.

```closure
docker rename <container-name> <container-name-to-what-you-want>
```
