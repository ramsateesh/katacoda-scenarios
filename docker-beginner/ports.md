# In this step we will learn

* Expose our container on a specific host port
* Test our application running in the container

###Expose our container on a specific host port

```
docker run -d --name my_nginx -p 8080:80 nginx
```

###Test our application running in the container

```
docker logs -f my_nginx
```
Now open a new terminal and run below commands...
```
curl localhost:8080

curl -X POST -d'{}' localhost:8080
```
watch what's happening in the other terminal
