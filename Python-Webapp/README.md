This is a web application created using Python Flask. It contains a Dockerfile which can be used to containerize it.
Clone this repository and in the folder run the following command

docker build . -t (Put any name here which you want to be the name of the docker image).
docker run (image name that you chose earlier).

## Test
Open a browser and go to URL

http://<IP>:5000                            => Welcome
http://<IP>:5000/how are you            => I am good, how about you?

https://hub.docker.com/repository/docker/ibad1112/python-webapp is the link to the image in dockerhub.
