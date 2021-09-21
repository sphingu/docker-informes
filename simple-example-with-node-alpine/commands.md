docker build -t one .
docker image ls
docker images
docker pull node:latest
docker run node:latest

docker ps -a (list all containers)
docker ps -a | grep c1 (list all containers having name c1)
docker start -i CONTAINER_ID (start container with container id or first few digit of container id)

docker exec -it CONTAINER_ID bash
docker exec -it -u john CONTAINER_ID bash (login with john user)
