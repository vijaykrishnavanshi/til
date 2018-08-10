# Install Jenkins in Docker Container 

Step 0: To install Jenkins on a docker container you need to make sure you have docker installed.

Docker is a freely available application that lets you install a fully-configured instance of Jenkins with a single command. To set up Docker on your computer, go to the Docker [installation page](https://www.docker.com/get-docker) and follow the instructions.

Step 1: Use Docker to Install Jenkins

This commands pulls the latest jenkins configured docker image to your local.

```closure
docker pull jenkins/jenkins:lts
```
This pulls the latest lts image of jenkins from the dockerhub.

Step 2: Run Neo4j Instance on default ports.

```closure
docker run -p 8080:8080 -p 50000:50000 jenkins/jenkins:lts
```

Admin panel is available on http://localhost:8080/

Step 3: Running it as a service.

```closure
docker run -d --publish=8080:8080 --publish=50000:50000 --name <container-name> jenkins/jenkins:lts
```

Host's 8080 & 50000 are mapped with the 8080 & 50000 ports of the docker container. You can change it as needed.

To get the initial admin password of jenkins from the running docker container - 

```closure
docker exec -i -t <container-name> /bin/bash
```

After this you should be inside the docker bash shell. See the contents of the file /var/jenkins_home/secrets/initialAdminPassword

```closure
cat /var/jenkins_home/secrets/initialAdminPassword
```

