# Docker commands
To build image run the following in your docker folder and name your container 

`docker build -t example_container_from_file .` 

Then you build a docker container 

`docker run -it example_container_from_file` 

To open a container in another terminal you can search the ID of the running container 

`docker ps` 

from there you will have the idea and then you can enter

`docker exec -it ID bash` 