
### Command List

##### Docker Quick Start Terminal
- Boot Docker VM.

##### Share Directory between Mac(Virtual Box host) and Docker-machine(Virtual Box image)
- A share directory is `/Users/Shared`.
- A root volume(/) is `tmpfs`.

##### `docker pull centos:7`
- Download centos 7 from Docker Hub.

##### `docker-machine ssh default`
- login docker VM.

##### `docker run centos:7 /bin/echo 'Hello '`
- Search centos:7.
- Download centos:7 if there isn't it.
- Run the container.
- --restart is reboot automatically.

##### `docker start [container id]`
- start the container after creating container image.

##### `docker stop [container id]`
- stop the container.

##### `docker inspect centos:7`
- show image info.

##### `docker image ls`
- show image list.

##### `docker search centos`
- search centos images that were created by Docker hub and  that are based on docker files on Github and Bitbucket.

##### `docker run -it --name "test2" centos /bin/bash`
- operate docker via command prompt.
- [User Name@Host Name Current Directory]Authentication($:user, #:root).

##### `docker run -d -p 8080:80 httpd`
- running on back ground.
- allocate localhost port(8080) to container port(80) using httpd image.
- check IP using docker-machine env or docker-machine ip (192.168.99.100)

##### `docker ps -a -f "name=xxxx"`
- show container list.

##### `docker rm [container id]`
- remove the container.

##### `docker attach [container id]`
- connect the container

##### `docker exec -it [container id] /bin/bash`
- connect the container using another process.

##### `docker-machine env`
- check docker info(IP, Name, Path etc.)

##### `docker build -t log-image /Users/Shared/Dockerfiles/log-image/`
- Create a log management container image.

##### `docker build -t web-image /Users/Shared/Dockerfiles/web-image/`
- Create a web server container image.

##### `docker run -it --name log-container log-image`
- Run a log management container.

###### `docker run -d --name web-container1 -p 80:80 --volumes-from log-container web-image`
###### `docker run -d --name web-container2 -p 8080:80 --volumes-from log-container web-image`
- Run  web server containers.

###### `docker exec -it web-container1 /bin/bash`
- Login web server containers.
