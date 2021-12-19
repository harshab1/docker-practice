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







