
## Hello Docker

To run your first docker container, check your OS architecture first:  
~$ `uname -m`{{execute}}

It should read: `x86_64` (~= `amd64`). This is the **traditional Linux arch that was supported by Docker**, but they have recently started to support multiple architectures ([github.com/docker-library/official-images#architectures-other-than-amd64](https://github.com/docker-library/official-images#architectures-other-than-amd64)).

If you're using the wrong architecture/manifest doesn't have this architecture listed, you should see something like this:  
*`no matching manifest for linux/amd64 in the manifest list entries`*

As such, pulling changed a bit because of manifests.

Pull the docker image locally:  
~$ `docker pull amd64/hello-world`{{execute}}

The image should now be listed:  
~$ `docker images`{{execute}}

Since you have downloaded your image, you can now run it (if you forget to pull, docker run will also do that for you):  
~$ `docker run amd64/hello-world`{{execute}}

The output for the image should appear. To check if the container is running:  
~$ `docker ps`{{execute}}

Nothing is listed, then look for containers that have been closed:  
~$ `docker ps -a`{{execute}}

## Useful commands in Docker

**Note**: Expect common commands like `ps`, `top`, `exec` to appear in similar contexts under Docker.

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

