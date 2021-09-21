# About Docker Containers

## run container in detached mode
- docker run -d IMAGE_NAME

### set container name
- docker run -d --name my-one IMAGE_NAME

## log command
- docker logs CONTAINER_ID

### follow logging output
- docker logs -f 123

### tail logging output
- docker logs -n 5 123

### timestamp logging output
- docker logs -n 5 -t 123

## set port
- docker run -d -p 80:5000 --name c1 IMAGE:TAG

## run command on running container
- docker exec -it c1 ls

## stop container
- docker stop c1

## start container
- docker start c1

## Remove container 
- docker container rm c1
- docker rm c1
- docker rm -f c1 (force running container to stop and remove)

## Docker volumes
- docker volume create my-data
- docker volume inspect my-data

- docker run ... -v my-data:/app/data ... (docker will create both of the if not exist(my-data on local as well as /app/data in container)) (will be created by root)
- docker run ... -v $(pwd):/app ... (volume as current working directory)

### Copy file
- docker cp CONTAINER_ID:/app/data/data.txt .
- docker cp test.txt CONTAINER_ID:/app/data/test1.txt