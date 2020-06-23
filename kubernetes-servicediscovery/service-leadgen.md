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

`kubectl -n leadgen get pods`{{execute}}

Verify that the service is up and running

`kubectl -n leadgen exec -it explorer -c explorer -- bash`{{interrupt}}{{execute}}

curl service

`curl -X GET http://app:8080/ShowEnv`{{execute}}

`curl -X GET http://app.leadgen:8080/ShowEnv`{{execute}}

`exit`{{execute}}