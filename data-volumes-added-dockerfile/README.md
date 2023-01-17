# Build container
docker build -t feedback-node:volumes .

# Start container in detached mode and remove when container is stopped
docker run -p 3000:80 --name feedback-app --rm feedback-node

# Named volumes
Good for data that needs to be persisted, not meant to be edited by the external world

# Start container with named volume
Named volumes will not be deleted when a container is shutdown. Unlike anonymous volumes.
docker run -d -p 3000:80 --rm --name feedback-app -v feedback:/app/feedback feedback-node:volumes

(will remove the container)
docker stop 

docker run -d -p 3000:80 --rm --name feedback-app -v feedback:/app/feedback feedback-node:volumes

(will have the data there bc of the name volume)
localhost:3000/feedback/awesome.txt

# Volumes
docker volume ls
```
DRIVER    VOLUME NAME
local     39865c72f963df847606501e52d3181b3242ad225cb5cbee30cab97c5257899c
local     feedback
```