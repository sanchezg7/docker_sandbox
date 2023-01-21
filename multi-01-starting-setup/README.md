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