# docker-practice
My docker sandbox

## Commands
```sh
docker pull busybox
docker run busybox echo "Hello, world!"
docker run -it sh
# in the container...'exit' to leave

# list containers
docker ps -a
# remove exited containers
docker rm $(docker ps -a -q -f status=exited)

# pull some images down
docker pull ubuntu # defaults to latest
docker pull golang:1.9.4 # latest doesn't seem to work...

# see images
docker images

# add a docker image to your images list
docker build -t pladdypants/golang . # this builds the local Dockerfile in this repo

# run it
docker run pladdypants/golang

# if you want to remove an image
docker rmi <image id>

# multi-containers
docker network inspect bridge

# create a network

# create a db container

# create app container


```

## Reference
- Tutorials:
  - https://docker-curriculum.com/
  - https://docs.docker.com/get-started/
- Images: https://hub.docker.com/
- How Tos:
  - https://www.digitalocean.com/community/tutorials/how-to-remove-docker-images-containers-and-volumes
