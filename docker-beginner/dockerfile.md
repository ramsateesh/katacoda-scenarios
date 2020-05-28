# In this step we will learn 

* Creating a Dockerfile
* Building an image from a Dockerfile

### Creating a Dockerfile
```
FROM nginx

COPY app/* /usr/share/nginx/html
```

### Building an image from a Dockerfile
```
docker build -t p3_nginx:0.1 .
```

Create a container

```
docker run -d -p 8080:80 --name p3_nginx p3_nginx:0.1

docker ps

curl localhost:8080
```

