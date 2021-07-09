1. docker version : Used to check the version of Server Docker Engine as well as Client Docker Engine.
2. docker run XXXX : Used to run a test container to see if docker is properly installed. Will run an instance of the XXXX on the docker host, if it already exists. Tf the image does not exist on the host, it will go to docker hub and pull the image the first time. For subsequent iteration the same image will then be used (not pulled every time).
3. docker ps : lists all the running containers and some basic info about them. Container Id and name is randomly assigned.
4. docker ps -a : shows all running or previously stopped containers as well as info about them
5. docker stop (Docker name or ID obtained from running docker ps command) : Stops the running container. If the command ran successfully the name or ID will be printed out
6. docker rm (Docker name or ID obtained from running docker ps command) : Deletes the container from memory to save space. If the command ran successfully the name or ID will be printed out. Can check again from docker ps -a
7. 
