# Install [Couchbase](https://www.couchbase.com/) in Docker Container

Step 0: Download and Install Docker

[Docker](https://www.docker.com) is a freely available application that lets you install a fully-configured instance of [Couchbase  Server](https://www.couchbase.com/) with a single command. To set up Docker on your computer, go to the Docker [installation page](https://www.docker.com/get-docker) and follow the instructions.

Step 1: Use Docker to Install Couchbase Server

Open a console window on your computer and enter the following command:

```clojure
docker run -d --name db -p 127.0.0.1:8091-8096:8091-8096 -p 127.0.0.1:11210-11211:11210-11211 couchbase
```

When you run the command, Docker downloads, installs, and configures Couchbase Server. This command binds 127.0.0.1:8091-8096 port to 8091-8096 port of the docker container so that we can access them as needed.

Now Admin panel of the couchbase server is available on 127.0.0.1:8091/

Step 2: Visit the admin panel at http://127.0.0.1:8091/

Note: You can make the couchbase available on you ip address as well just change the binding from 127.0.0.1:* to 0.0.0.0:* Then you can access your admin panel on your ip:8091.
