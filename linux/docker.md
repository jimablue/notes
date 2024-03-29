### Docker Container

*Containers* virtualize the necessary part of host operating system only (unlike virtual machine which creates an entire guest OS).

*Containers* are just *imagines* in running state.

*Images* are files that act as the template for creating containers(like a frozen, read-only copy of a container)
*images* can be exchanged throught registry

An image *registry* is a centralized place where you can upload your images and can also download images created by others.

### Docker Architecture 

Docker engine:

Docker Client -> REST API -> Docker Daemon

### Common Commands
`docker <object> <command> <options>`  

object: `container`, `image`, `network`, `volume`  
command: `run`, `create`,`start` ,`restart` ,`rm`, `prune`(remove all dangling container), 
options:  `--publish/-p` option for port mapping.  `--publish <host port>:<container port>`  
`--detach/-d` keep container running in the background  
`--rm` remove after it's stopped  
`--name` name for container  
`-it`   

`docker container run <image name>`  
`docker container run --publish 8080:80 fhsinchy/hello-dock`  
Above means any request sent to port 8080 of your host system will be forwarded to port 80 inside the container‌.

List containers  
`docker container ls` add `-a` to list all(including not running)

### execute commands inside container
`docker container run <image name> <command>`

### executable images

bind mount: two way data binding between the local file system directory and another directory inside a container
`--volume <local file system directory absolute path>:<container file system directory absolute path>:<read write access>`


### Docker Image manipulation

A `Dockerfile` is a collection of instructions that, once processed by the daemon, results in an image. 