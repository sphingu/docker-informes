# Docker Compose 

## Cleanup

### All bellow command are same and use to remove all(-a) container using container id get by filter (-q) 
- docker container rm -f $(docker container ls -a -q) 
- docker container rm -f $(docker container ls -aq)   
- docker container rm -f $(docker ps -aq)   
- docker rm -f $(docker ps -aq)   

### Remove all images
- docker image rm -f $(docker image ls -aq)

## Build
- docker-compose build (will build docker images)
- docker-compose build --no-cache (will build docker images without cache)

## Up
- docker-compose up (will build image if not build the do run container from it)
- docker-compose up --build (will always build docker image (build+up))
- docker-compose up -d (detached mode)

## Down
- docker compose down (will stop and remove containers) (images will kept as it is)


## Networking
- docker network ls
  - bridge
  - host
  - none
  - diviser_default
- DNS Resolver based on name of service in docker-compose file.
- can check network through "ping api" on web container shell.

## Logs
- docker compose logs
- docker compose logs -f -t
