Let's create leadgen service

Below command creates following:

* Namespace (leadgen)
* Deployment (api-guid-generator)
* Service (api-guid-svc)
* Static pod (explorer)

`kubectl apply -f service-leadgen.yaml`{{execute}}

See what got created

`kubectl -n leadgen get all`{{execute}}

Wait until all pods get created

`kubectl -n leadgen get pods`{{execute}}

Verify that the service is up and running

`kubectl -n leadgen exec -it explorer -c explorer -- bash`{{interrupt}}{{execute}}

curl service

`curl -X GET http://api-guid-svc:8080`{{execute}}

`curl -X GET http://api-guid-svc.leadgen:8080`{{execute}}

`exit`{{execute}}