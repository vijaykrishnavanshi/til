# Copy Files from [Docker](https://www.docker.com/) Container to Host

The docker cp command can be used to copy files. One specific file can be copied like:

```closure
docker cp <source-filepath-from-host> <container-name>:<target-filepath-on-container>
docker cp <container-name>:<source-filepath-on-container> <target-filepath-on-host>
```

Multiple files contained by the folder src can be copied into the target folder using:

```closure
docker cp <source-directory-on-host> <container-name>:<target-directory-on-container>
docker cp <container-name>:<source-directory-on-container> <target-directory-on-host>
```
