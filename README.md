# Build the image
Create an image, given the directory to look for the Dockerfile
`docker build .`

```
[+] Building 5.3s (9/9) FINISHED
 => [internal] load build definition from Dockerfile                                           0.0s
 => => transferring dockerfile: 332B                                                           0.0s
 => [internal] load .dockerignore                                                              0.0s
 => => transferring context: 2B                                                                0.0s
 => [internal] load metadata for docker.io/library/node:latest                                 0.0s
 => [1/4] FROM docker.io/library/node                                                          0.2s
 => [internal] load build context                                                              0.0s
 => => transferring context: 2.26kB                                                            0.0s
 => [2/4] WORKDIR /app                                                                         0.0s
 => [3/4] COPY . /app                                                                          0.0s
 => [4/4] RUN npm install                                                                      4.9s
 => exporting to image                                                                         0.1s
 => => exporting layers                                                                        0.1s
 => => writing image sha256:f15914fc60fef111c792bdec41e835973c5da3350ed946574d0bf35c07cc2df9   0.0s
```

# Create a container and publish to a port
`docker run -p 3000:80 12345`

# Restart a container
docker start <name>
It will retain the bound port.

# Attaching to an already-running Container
docker attach <containerid>

# Remove created containers
docker rm

# Stop a container
docker stop <container id>

# Image
## List images
docker images

## Remove Image
docker rmi <image id>

## Prune images
docker image prune -a

