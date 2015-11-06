 run the redis container:

 docker run --name redis-container -d redis

 run the node app with a link to a redis container:

 docker run -it --link redis-container:redis -p 8000:8000 -v /home/colby/code/sample-docker-node/script:/usr/src/app colby-node bash

 checkout persistent storage for redis:
 https://hub.docker.com/_/redis/

 docker flags with run:
 -i connects STDIN to newly created container
 -t interactive terminal (requires something like bash at end)
 -d detach container
 -p PORT:PORT to map a port 
 --link name-of-container:ALIAS_of_container

docker flag with build:

docker flag with rm:
-v when doing an rm command will get rid of any volumes



 to detach from within a container that was not started with a -d flag: ctrl + p + q
 to attach to a running docker container: docker exec -it <container id> bash

 docker logs --tail 10 -f <container id>

remove all docker containers: docker rm $(docker ps -qa)

