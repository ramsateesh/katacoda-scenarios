#In this step we will learn 

* pull an image
* start a container with the image
* inspect image
* tag image
* remove image

###Pull a docker image

```
docker pull mcr.microsoft.com/dotnet/core-nightly/sdk:2.2
```

###Start a container
```
docker run --it mcr.microsoft.com/dotnet/core-nightly/sdk:2.2

root@<container_id>:/# dotnet --info

root@<container_id>:/# ps -ef

root@<container_id>:/# cat /etc/passwd | grep root

root@<container_id>:/# exit
```

###Inspect docker image

```
docker inspect mcr.microsoft.com/dotnet/core-nightly/sdk:2.2
```

###Tag Docker Image

```
docker tag mcr.microsoft.com/dotnet/core-nightly/sdk:2.2 mcr.microsoft.com/dotnet/core-nightly/sdk:2.2-prospa

docker images
```

###Remove Docker Image

```
docker rmi mcr.microsoft.com/dotnet/core-nightly/sdk:2.2

docker rmi mcr.microsoft.com/dotnet/core-nightly/sdk:2.2-prospa
```