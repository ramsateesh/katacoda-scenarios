#In this step we will learn 

* start/run a container
* see what containers are running
* test out application running in the container
* explore the container
* inspect the container
* tail logs of our container 
* stop our container
* delete our container

###Let's start with a dotnet sdk container

```
docker run -d --name my_nginx nginx
```

###See what container is running

```
docker ps 
```

###Explore our container

```
docker exec -it my_nginx /bin/bash
```

###Inspect our container

```
docker inspect my_nginx
```

###Tail logs of our container

```
docker logs -f my_nginx
```

###Stop our container

```
docker stop my_nginx
```

###Remove container

```
docker rm my_nginx
```