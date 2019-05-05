# Install [Neo4j](https://neo4j.com/) in [Docker](https://www.docker.com) Container

Step 0: To install Neo4j on a docker container you need to make sure you have docker installed.

Docker is a freely available application that lets you install a fully-configured instance of Neo4j with a single command. To set up Docker on your computer, go to the Docker [installation page](https://www.docker.com/get-docker) and follow the instructions.

Step 1: Use Docker to Install Neo4j Graph Database

This commands pulls the latest neo4j configured docker image to your local.

```closure
docker pull neo4j
```

Step 2: Run Neo4j Instance on default ports.

```closure
docker run \
    --publish=7474:7474 --publish=7687:7687 \
    --volume=$HOME/neo4j/data:/data \
    neo4j
```

$HOME/neo4j/data is the directory where neo4j container persists its data. Delete it and the state of the container is reset.

Step 3: Running it as a service.

```closure
docker run -d --publish=7474:7474 --publish=7687:7687 --volume=$HOME/neo4j/data:/data --name neo4j-container neo4j
```

neo4j-container is the name of the container. Host's 7474 & 7687 are mapped with the 7474 & 7687 ports of the docker container.

Pass --env=NEO4J_AUTH=none flag to disable authentication.
