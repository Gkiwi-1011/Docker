### Docker Compose
- Centrally manage compose of plural docker images.(DB, Web, AP, Frontend etc)
- Using a docker compose yaml file to manage compose of plural docker image.

##### `docker run -it --name apserver -d --link dbserver:db centos:7 /bin/bash`
- Link AP server to DB server using alias db.
-  

##### `set | grep PG`
- Check env on AP server container.

##### Install a docker compose on docker-machine as a root authentication.
- Refer to `https://github.com/docker/compose/releases`

##### image syntax
- Specify a image name.

##### build syntax
- Specify a Dockerfile directory.

##### `docker-compose -f COMPOSE_FILE_PATH up`
- Create & Run the compose of dockers.

##### `docker-compose scale web-container=10`
- Scale out 20 web-containers

