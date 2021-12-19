## Docker Intro:

docker version --> first command to check installation 

docker info --> configuration values

docker --> list of commands

docker run image-name over-riding-command --> the overriding command will replace the default command that image would execute

docker ps --> list  the containers

docker ps --all --> all the containers started up

docker run = docker create + docker start 

docker start container-id --> restart the stopped or exited container, reissue the overriding command that was used while creating the container in first place

docker system prune --> will delete all the containers, networks, dangling images and build cache

docker logs container-id --> logs of the container thats running or stopped as well

docker stop container-id  and docker kill container-id --> minor differnece between the both commands. stop triggers the OS to stop the service without objecting to do clean up or saving the files before stopping where as kill will make the stopping immediately

docker exec -it container-id command --> to run commands inside a container, command processors can be sh, bash, poweshell, zsh

docker run -it image-name command-processor --> starting a command-processor immediatly with container

## Docker file:

Three important components: 1. Base Image 2. Run commands to install additional commands,  3. command to run on container start-up

During each step, the image is updated with the instructions/commands from the previous step and the snapshot is passed to next step

docker build . --> builds the image from the Dockerfile

Docker gets its performance by using the cache to build temporary intermediate images

Tagging the image is important to identify a image based on the custom name rather than ID. The fromat is "Docker-ID/project-name:version". Argument "-t". 

In the dockerfile the working directory is setup using the command "WORKDIR", this will avoid deleting the files or make unintended changes in the default root directory

docker build -f docker-file-name --> dockerfile with name differnet to default Dockerfile

## Docker compose:

Docker compose will manage multiple images and provide a network infrastructure between the containers

docker run image-name ==> docker-compose up --> start all the containers

docker build . and docker run image-name ==> docker-compose up --build 

docker-compose down --> stop all the containers

Restart policy: If there's a failure in container starting and crashing, restart policy will specify how to deal with it in four possible ways: no (default), always, on-failure and unless-stopped

docker-compose ps --> containers specific to docker-compose file in that directory












