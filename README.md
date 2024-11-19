# Web service with load balancer
# purpose of teh project
This project is based on a simple web service accessed through a load balancer using Docker.
It includes two containers
1. one for the web service
2. other one for the load balancer

# First we have created the Dockerfile1 and Dockerfile2 

# Dockerfile1 is for node 

# Dockerfile2 is for nginx

# Ran below command to check the dockefiles are creating the images or not (This is only for checking purpose)
docker -t node:v1.1.0 build -f Dockerfile1 .

docker -t nginx:v1.1.0 build -f Dockerfile2 .

# We have created the docker-compose file

# We have used the below command to delete the unused resources
docker system prune

# Used below command to run the docker-compose.yml file 
docker-compose up

# checked the docker images 
docker images 

# checked the docker running containers
docker ps 

# go to the browser and paste below url, It will access the web service through nginx load balancer
http://localhost:8081/

# Used below command to stop the containers
docker-compose down