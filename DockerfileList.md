### Dockerfile
- Create a Docker Container
- Configure a Infrastructure configuration
- Configure OS
- Install & Configure Middleware
- Deploy applications


#### FROM
- specify a base image file.

#### RUN
- execute command to create an image file.
- install middle wares.
- configure middle wares.
- execute command.
- You want to execute commands as shell format.
- Other than that(like a bash format etc.), you execute commands as exec format.
- RUN should be used as one line commands to prevent from creating many layer.

##### ADD
- configure middle wares.


#### CMD
- execute commands in a container after creating the container.
- run httpd as deamon.

#### ONBUILD
- deploy applications.
1. create a Dockerfile.base for a base image.(define ONBUILD)
2. `docker build -t base -f Dockerfile.base .` (The current directory include Dockerfile.base.)
3. create a deploy file (tar file using `tar -cvf xxx.tar DIR`.) & Dockerfile that is FROM the above base image.
4. `docker build -t web .` (The current directory includes the Dockerfile and the tar file.)

