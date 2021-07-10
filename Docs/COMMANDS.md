1. docker version : Used to check the version of Server Docker Engine as well as Client Docker Engine.
2. docker run (image name) : Used to run a container from an image. Will run an instance of the image on the docker host, if it already exists. Tf the image does not exist on the host, it will go to docker hub and pull the image the first time. For subsequent iteration the same image will then be used (not pulled every time).
3. docker ps : lists all the running containers and some basic info about them. Container Id and name is randomly assigned.
4. docker ps -a : shows all running or previously stopped containers as well as info about them
5. docker stop (container name or ID obtained from running docker ps command) : Stops the running container. If the command ran successfully the name or ID will be printed out. Can stop multiple containers by entering their short ID after space
6. docker rm (container name or ID obtained from running docker ps command) : Deletes the container from memory to save space. If the command ran successfully the name or ID will be printed out. Can check again from docker ps -a. Can remove multiple containers by entering their short ID after space
7. docker images : list the images present on our host and their sizes
8. docker rmi (image name) : Removes the image from the host. A new one can be downloaded if you want to upgrade. Ensure no containers are running from that image before attempting.
9. docker pull (image name) : Pulls the image from docker hub to your host but does not run the container unlinke docker run
#### Appending a Command
10. docker run ubuntu sleep 5 : Any command can be appended by adding commands in front of it for example in this command the container starts and goes to asleep for 5 seconds. After it wakes up the container exits because there is no process running
#### Executing a command inside a docker container
10. docker exec (container name) (command) - example docker exec sleeping_snippity cat /etc/os-release
#### Attaching or detaching a docker container
11. docker run -d (image) : Will run the container in a detached mode giving you the control of the CLI without forcing it to exit
12. docker attach (id or name) : To attach the container back in CLI
13. docker run -it (image) : Used to automatically log in to the container when it is run
14. 
