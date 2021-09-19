docker build -t testd .
docker build -t testd:1.0.0 . (build image with tag)
docker run -it testd
docker run -it testd bash (not available for alpine linux)
docker run -it testd sh (work with alpine)

apk package manage available in alpine instead of apt
adduser available in case of alpine instead of useradd

docker run testd npm start

CMD npm start => will start new shell(/bin/sh) (called Shell form)
CMD ["npm", "start"] => will run in existing shell (called Execute form)

CMD => can be override in docker run command directly 
ENTRYPOINT => need to specify (--entrypoint) to override (docker run -it testd --entrypoint sh)

docker history testd (to see docker image layers information)

dangling images as <none>

docker image prune
docker container prune
docker image rm NAME/ID

docker images remove testd:1.0.0
docker image tag testd:1.0.0 testd:2.0.0  (update image tag)

// image push to docker hub
docker login
docker push testd:1.0.0

// image save as zip file
docker image save -o testd.tar testd:1.0.0

// load image through zip
docker image load -i testd.tar