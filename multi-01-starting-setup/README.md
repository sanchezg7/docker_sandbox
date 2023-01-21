# Multiple Container Project
- frontend
- backend
- mongodb 

Mongodb must persist data, it must also create a user creds as specified.

## Mongodb
Basic form of starting the container on a specific port.
`docker run --name mongodb --rm -d -p 27017:27017 mongo`

## Node Backend
docker build -t goals-node

## run
docker run --name goals-backend --rm goals-node

## stop
docker stop 782

## run and publish the correct port 
docker run --name goals-backend --rm -d -p 80:80 goals-node

## React frontend
docker build -t goals-react .
docker run --name goals-react --rm -d -p 3000:3000 goals-react

# Networking
Creating a docker network to formally put all the respective containers in to communicate.
`docker network create goals-net`
hash is provided

## Run a container in the respective network
`docker run --name mongodb --rm -d --network goals-net mongo`
Backend
`docker run --name goals-backend --rm -d --network goals-net goals-node`