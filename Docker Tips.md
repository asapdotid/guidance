##If you want to cleanup docker images and containers

CAUTION: this will flush everything


###stop all containers

> docker stop $(docker ps -a -q)

###remove all containers

>docker rm $(docker ps -a -q)

###remove all images

>docker rmi -f $(docker images -a -q)
