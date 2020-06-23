Let's create leadgen service

Below command creates following:

* Namespace (leadgen)
* Deployment (app-deployment)
* Service (app)
* Static pod (explorer)

`kubectl apply -f service-leadgen.yaml`{{execute}}

See what got created

`kubectl -n leadgen get all`{{execute}}

Wait until all pods get created

`kubectl -n leadgen get pods -o wide -w`{{execute}}

###Logs

Let's monitor the logs for leadgen is a new terminal

`kubectl logs -f -n leadgen -l component=app --all-containers=true`{{execute T3}}

### Test app Service

exec to explorer to test our app service in leadgen

`kubectl -n leadgen exec -it explorer -c explorer -- bash`{{execute interrupt}}

curl app service

`curl -X GET http://app:8080/ShowEnv`{{execute}}

`curl -X GET http://app.leadgen:8080/ShowEnv`{{execute}}

`curl -X GET http://app.leadgen:8080/ShowGuid`{{execute}}

`exit`{{execute}}