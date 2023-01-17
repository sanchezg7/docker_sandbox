# Container Networking
The project to work with cross-container communication and www communication

# Build the image
Note that latest is implicit
docker build . -t favorites-node:latest

# Instantiate a container from the image
docker run --name favorites -d --rm -p 3000:3000 favorites-node
---  

Containers can communicate to WWW by default.

`host.docker.internal` to communicate to other services on the local machine
mongodb:/host.docker.internal:27017/swfavorites

# Using mongo image
It's already provided in dockerhub

## Manually find IP address (brittle approach)
docker run mongo will create a container with the image  
`docker inspect <container name>`  
`docker inspect mongodb`

Find the ip address and put it into the application source code

# Docker networks
Can add a container to the network
`docker run --network my_network`
This will allow containers to talk to each other

## Attach mongo to a docker network
### Create the network first
docker network create favorites-net
### Create container and attach to network
docker run -d --name mongodb --network favorites-net mongo