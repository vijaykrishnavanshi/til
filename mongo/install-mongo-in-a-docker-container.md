# Install [Mongo](https://www.mongodb.com/) in [Docker](https://www.docker.com/) Container

Step 0: Download and Install Docker

Docker is a freely available application that lets you install a fully-configured instance of MongoDB with a single command. To set up Docker on your computer, go to the Docker [installation page](https://www.docker.com/get-docker) and follow the instructions.

Step 1: Use Docker to Install Mongo 3.4

Open a console window on your computer and enter the following command:

```clojure
docker run -d -p 127.0.0.1:27017:27017 -p 127.0.0.1:28017:28017 --name mongo-3.4 mongo
```

When you run the command, Docker downloads and installs Mongo on Docker Container with a name - mongo-3.4. This command binds 127.0.0.1:27017 port to 27017 port of the docker container so that we can access them as needed.

Step 2: You can use [Robomongo](https://robomongo.org/) / mongo shell to confirm if the mongo is correctly setup.

Note: You can make the mongo available on you ip address as well just change the binding from 127.0.0.1:* to 0.0.0.0:*
