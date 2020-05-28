#In this step we will learn

* How to pass environment variables to our containers
* How to pass them using a file
* Which is better/secure ?

### How to pass environment variables to our containers
```
docker run -d --name my_nginx_env --env DOMAIN=platform nginx

docker exec -it my_nginx_env bash
```

### How to pass them using a file
```
docker run -d --name my_nginx_env_file --env-file env.list nginx

docker exec -it my_nginx_env_file bash
```

### Which is better/secure ?
```
ps aux | grep nginx
```

### Cleanup

```
docker stop my_nginx_env
docker stop my_nginx_env_file

docker rm my_nginx_env
docker rm my_nginx_env_file
```