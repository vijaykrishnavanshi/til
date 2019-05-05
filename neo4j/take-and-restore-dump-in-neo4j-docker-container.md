# Take and restore dump of [Neo4j](https://neo4j.com/) Database in [Docker](https://docker.com) Container

Step 0: List all the docker containers that are currently running on your machine using the following command.

```closure
docker ps
```

Output should look like a table. Note the container id that has neo4j database.

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

docker run --volume=$HOME/neo4j/data:/data --name=myname-neo4j -it neo4j -c /bin/bash

docker run --name neo4j-dump --mount type=bind,source=$HOME/neo4j/data,target=/data neo4j bin/neo4j-admin dump --database=heidelberg.db --to=/heidelberg.db.dump
