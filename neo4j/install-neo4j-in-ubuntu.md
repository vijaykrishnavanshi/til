# Install Neo4j in Ubuntu 

Step 0: To install Neo4j on Debian you need to make sure that you have Java 8 Runtime is installed.

These commands should do the trick.

```closure
sudo add-apt-repository ppa:webupd8team/java
sudo apt-get update
sudo apt-get install oracle-java8-installer
```

Step 1: Add the repository

```closure
wget -O - https://debian.neo4j.org/neotechnology.gpg.key | sudo apt-key add -
echo 'deb https://debian.neo4j.org/repo stable/' | sudo tee -a /etc/apt/sources.list.d/neo4j.list
```

Step 2: Update the repositories.

```closure
sudo apt-get update
```

Step 3: Installing

```closure 
sudo apt-get install neo4j=1:3.4.1
```

