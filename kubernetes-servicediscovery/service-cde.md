Let's create cde service

Below command creates following:

* Namespace (cde)
* Deployment (api-guid-generator)
* Service (api-guid-svc)
* Static pod (explorer)

`kubectl apply -f service-cde.yaml`{{execute}}

See what got created

`kubectl -n cde get all`{{execute}}

Wait until all pods get created

`kubectl -n cde get pods`{{execute}}

Verify that the service is up and running

`kubectl -n cde exec -it explorer -c explorer -- bash`{{interrupt}}{{execute}}

curl service

`curl -X GET http://api-guid-svc:8080`{{execute}}

`curl -X GET http://api-guid-svc.cde:8080`{{execute}}

`exit`{{execute}}