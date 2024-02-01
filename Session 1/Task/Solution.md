Q1) `docker images` or `docker image ls`

Q2) `docker run alpine cat /etc/hostname`   or  you can create a container and run `docker exec` on it

```
docker run alpine sleep 100
docker exec <contianer_ID/name> cat /etc/hostname
```

Q3) `docker pull ubuntu:noble`

Q4) `docker run -d erseco/alpine-php-webserver`

Nothing appears when visiting `localhost:8080`

Q5) `docker run -d -p 55:8080 erseco/alpine-php-webserver`

Q6) ![](imgs/Q6.png)

Q7) 
```
docker ps
    
docker stop 26de or docker stop elegant_boyd

docker rm 26de or docker rm elegant_boyd
```