# docker cheat sheet

Project to start practicing with docker containers and docker-compose. To begin with the learning enviroment run in a console inside the project:

## Useful docker commands

### Docker images manipulation

Login to docker public registry (docker-hub)

`docker login`

Pull an image from docker-hub

`sudo docker image pull python:3.4-alpine`

List all docker images downloaded either from docker-hub or another registry

`docker image ls`

Remove a docker image

`docker image rm <image-id>`

Remove a docker image forcefully

`docker image rm -f <image-id>`

Inspect a docker image

`docker image inspect <image-id>:<my-tag>`

See size of intermediate images that make up your image

`docker image history <image-id>:<my-tag>`

Remove one or more docker images

`docker rmi <image-id>`

Delete all docker images

`docker rmi $(docker images -q)`

Forcefully delete all docker images

`docker rmi $(docker images -q) --force`

Export docker image into a tar.gz file

`docker save <grupo>/<name>:<version> | gzip -9 > <grupo>_<name>_<version>.tar.gz`

Load docker image from a tar.gz file into local repository

`gunzip -c -k <grupo>_<name>_<version>.tar.gz | docker load`

Remove docker dangling images -> [More Info of Dangling images](https://www.projectatomic.io/blog/2015/07/what-are-docker-none-none-images/)

`docker rmi $(docker images -f "dangling=true" -q)`

### Docker container manipulation

Run a container with interactive processes (like a shell)

`docker run -it <image-id>`

Run a container with interactive processes (like a shell) in a deattached mode

`docker run -d -it <image-id>`

Attach a deatacched container -> [More Info](https://docs.docker.com/engine/reference/commandline/attach/)

`docker attach <container-id>`

Run a container and share bind mount between host and container

`docker run -d -P --name frontend -v /src/webapp:/opt/webapp -v db_volume:/var/db_data frontend`

`-d` Deattached mode\
`-P` Publish all ports exposed in Dockerfile\
`--name` Container name to easily identify it instead of using container id\
`-v` mount `/src/webapp` directory on host to the `/opt/webapp` on container\
`-v` create and/or mount `db_volume` on host to the `/var/db_data` on container\ 
`frontend` Image name

Run a container named `friendlyhello` in the background (deattached mode) and publish the port `4000` in the host and maps it to port `5000` inside the container

`docker run -d -p 4000:5000 friendlyhello`

List all running containers

`docker ps`\
`docker container ls`\
`docker container ps`

List all containers

`docker ps -a`

Example Output:

```bash
CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS                            NAMES
f263b6710fdc        friendlyhello       "python app.py"     11 seconds ago      Up 8 seconds        80/tcp, 0.0.0.0:4000->5000/tcp   kind_chaum
```

List running container IDs

`docker container ls -q`

List history of containers (Not only just the running ones)

`docker container ls --all`

Example Output

```bash
CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS                      PORTS                            NAMES
f263b6710fdc        friendlyhello       "python app.py"     3 minutes ago       Up 3 minutes                80/tcp, 0.0.0.0:4000->5000/tcp   kind_chaum
103ed3c668e1        friendlyhello       "python app.py"     18 minutes ago      Exited (0) 7 minutes ago                                     infallible_ride
46d16b7d611e        friendlyhello       "python app.py"     24 minutes ago      Exited (0) 18 minutes ago                                    distracted_einstein
9f150bd485c7        hello-world         "/hello"            2 hours ago         Exited (0) 2 hours ago                                       optimistic_ardinghelli
```

List containers in quiet mode

`docker container ls -aq`

Example Output

```bash
f263b6710fdc
103ed3c668e1
46d16b7d611e
9f150bd485c7
```

View approximate size of a running container

`docker container ls -s`

View approximate size of old containers

`docker container ls -a -s`

See log of a container

`docker logs <container-id>`

To see the log output of a running container

`docker logs --follow <container-id>`

Override entrypoint

`docker run --entrypoint <new-entrypoing> <image-id>`

Lists all files inside /code/ folder inside container with id "5674f4dd7d27"

`docker exec -it 5674f4dd7d27 ls /code/`

Start a shell terminal inside the container with id "5674f4dd7d27"

`docker exec -i -t 5674f4dd7d27 sh`

Stop a running container

`docker stop <container-id>`

or

`docker kill <container-id>` (It does not attempt to shut down the process gracefully first)

Stop all running containers

`docker stop $(docker ps -aq)`

or

`docker kill $(docker ps -aq)` (It does not attempt to shutdown the process gracefully first)

Remove one or more stopped containers

`docker rm <container-id>`

Delete all stopped containers

`docker rm $(docker ps --filter status=exited -aq)`

### Docker volumes manipulation

List available volumes

`docker volume ls`

Example Output:

```bash
DRIVER              VOLUME NAME
local               55bd8f88e1307ab51f620bbb3b9578ceca8edbf0fee29b1fa2f5c62cad34c193
local               jenkins_home
local               netbox-docker_netbox-media-files
local               netbox-docker_netbox-nginx-config
local               netbox-docker_netbox-postgres-data
local               netbox-docker_netbox-redis-data
local               netbox-docker_netbox-report-files
local               netbox-docker_netbox-static-files
```

Inspect a volume

`docker volume inspect jenkins_home`

Example Output:

```json
[
    {
        "CreatedAt": "2019-04-22T12:20:54-03:00",
        "Driver": "local",
        "Labels": null,
        "Mountpoint": "/var/lib/docker/volumes/jenkins_home/_data",
        "Name": "jenkins_home",
        "Options": null,
        "Scope": "local"
    }
]
```

Remove a volume

`docker volume rm jenkins_home`

### Docker networks manipulation

TBC.

### Docker services and stack manipulation

List stacks or apps

`docker stack ls`

Run the specified Compose file

`docker stack deploy -c <composefile> <appname>`

List running services associated with an app

`docker service ls`

List tasks associated with an app

`docker service ps <service>`

Inspect task or container

`docker inspect <task or container>`

Tear down an application

`docker stack rm <appname>`

Enable swarm mode on the host

`docker swarm init`

Enable swarm mode on the host and advertise address `192.168.99.11`

`docker swarm init --advertise-addr 192.168.99.11`

Join a machine in the swarm as worker

`docker swarm join --token <token_id> <myvm ip>:<port>`

Take down a single node swarm from the manager

```bash
docker swarm leave
docker swarm leave --force
```

List all the nodes in a swarm

`docker node ls`

## Useful docker-compose commands

Build and run your app with compose

`docker-compose up`

Build and run your app with compose forcing to build images based on a Dockerfile

`docker-compose up --build`

Stop the application

`docker-compose down`

Note: docker-compose commands have to be runned inside the directory where docker-compose.yml resides

## Useful docker-machine commands

Create a machine called **myvm1** (Future node of a swarm cluster)

`docker-machine create --driver virtualbox myvm1`

Start a machine

`docker-machine start myvm1`

Stop a machine

`docker-machine stop myvm1`

Remove a machine

`docker-machine rm myvm1`

Lists machines (asterisk shows which VM this shell is talking to)

`docker-machine ls`

Show environment variables and command for myvm1

`docker-machine env myvm1`

Command to connect shell to myvm1

`eval $(docker-machine env myvm1)`

Disconnect shell from VMs, use native docker

`eval $(docker-machine env -u)`

Run commands inside a machine through ssh

`docker-machine ssh myvm1 "docker swarm init --advertise-addr <myvm1 ip>"`