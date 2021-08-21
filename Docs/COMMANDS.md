#### Basic Commands :
1. docker version : Used to check the version of Server Docker Engine as well as Client Docker Engine.
2. docker run (image name) : Used to run a container from an image. Will run an instance of the image on the docker host, if it already exists. Tf the image does not exist on the host, it will go to docker hub and pull the image the first time. For subsequent iteration the same image will then be used (not pulled every time).
3. docker ps : lists all the running containers and some basic info about them. Container Id and name is randomly assigned.
4. docker ps -a : shows all running or previously stopped containers as well as info about them.
5. docker stop (container name or ID obtained from running docker ps command) : Stops the running container. If the command ran successfully the name or ID will be printed out. Can stop multiple containers by entering their short ID after space.
6. docker start (container name or id) : Starts the stopped container.
7. docker rm (container name or ID obtained from running docker ps command) : Deletes the container from memory to save space. If the command ran successfully the name or ID will be printed out. Can check again from docker ps -a. Can remove multiple containers by entering their short ID after space.
8. docker images : list the images present on our host and their sizes.
9. docker rmi (image name) : Removes the image from the host. A new one can be downloaded if you want to upgrade. Ensure no containers are running from that image before attempting.
10. docker pull (image name) : Pulls the image from docker hub to your host but does not run the container unlinke docker run.
11. docker run -it (image) : Used to automatically log in to the container when it is run.
12. docker run --name (setyournamehere) (image) : Used to give the container a user specified name.
13. docker run (image):tag : To run a container of an image with a specifc version where the tag is used to specify the version number. If tag is not specified docker will consider default tag to be latest i.e. format will be (image:latest).
#### Appending a Command
13. docker run ubuntu sleep 5 : Any command can be appended by adding commands in front of it for example in this command the container starts and goes to asleep for 5 seconds. After it wakes up the container exits because there is no process running.
#### Executing a command inside a docker container :
14. docker exec (container name) (command) - example docker exec sleeping_snippity cat /etc/os-release.
#### Attaching or detaching a docker container :
15. docker run -d (image) : Will run the container in a detached mode giving you the control of the CLI without forcing it to exit.
16. docker attach (id or name) : To attach the container back in CLI.
#### Basic Commands (Continued) :
17. docker run -p dockerhostportnumber:containerportnumber (image) : The -p command is used for port forwarding your docker host port to your container port. The docker host is that machine or VM in which docker is installed.  
18. docker logs (name or id) : Shows the logs of the container irrespective of whether they are running or stopped.
19. docker exec -it (container name or id) (command mostly /bin/bash) : To interact with the container terminal. Mostly a container is made up of light weight images so most of the commands might not be available.
20. docker network ls : Displays the docker networks
21. docker network create (network name) : Create a network in docker
22. docker run -i (image) : Here -i stands for interactive mode, used if you want to give an input to docker container. -t means terminal mode.
23. docker run -v (/directory in docker host):(/directory in container) (image) : To persist data after container removal one can map a directory inside the container to a directory inside the docker host. This way when the docker container runs it will implicitly mount the external directory to a folder inside the docker container.
24. docker inspect (container name or id) : A way to inspect the configuration of a container in JSON format.
25. docker history (image) : Shows the building layers of the images.
26. docker build Dockerfile -t : (name of the docker image) 
