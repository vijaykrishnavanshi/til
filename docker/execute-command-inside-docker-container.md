# Execute command in a running Docker Container

Step 0: List all the docker containers that are currently running on your machine using the following command.

```closure
docker ps
```

Output should look like a table. Note the container id that you want to execute command into.

Step 1: Execute the command.

```closure
docker exec -it <container-id/container-name> <command>
``` 

Best way to explore the file system inside docker is to connect a shell.

```closure
sudo docker exec -ti <container-id/container-name> /bin/bash
```

