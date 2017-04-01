
## Useful commands in Docker

Search [hub.docker.com](https://hub.docker.com/) for a certain image:
`docker search <name>`

Download the image locally (for later use):
`docker pull <name>`

Check configuration json for a specific instance:
`docker inspect <name>`

Check logs for an instance:
`docker logs <name>`

### Docker instance control commands

Run a docker container for `node` image (if it hasn't been found locally, it will automatically `pull`):
`docker run -t node`{{execute}}

Every time an object gets instantiated, it will be assigned a new id (**alphanumeric**, **12 characters**), and a readable name (`name1_name2`). Usually you would prefer using the readable name for management.

Start a previously instantiated container (run has been done before, that container is found in `docker ps -a`):
`docker run -t hello-world`{{execute}}
`docker start <name>`

Connect to a container (attach a bash to the docker instance and login):
`docker exec -it <name> bash`

Stop a currently active container (container is listed in `docker ps`):
`docker stop <name>`

