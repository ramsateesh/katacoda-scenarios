Let's create cde service

Below command creates following:

* Namespace (cde)
* Deployment (api-deployment)
* Service (api)
* Static pod (explorer)

`kubectl apply -f service-cde.yaml`{{execute}}

See what got created

`kubectl -n cde get all`{{execute}}

Wait until all pods get created

`kubectl -n cde get pods`{{execute}}

Verify that the service is up and running

`kubectl -n cde exec -it explorer -c explorer -- bash`{{interrupt}}{{execute}}

###Logs

Let's monitor the logs for cde is a new terminal

`kubectl -n cde logs -f $API_POD_1`{{copy}}

### Test api Service

curl service

`curl -X GET http://api:8080/api/guid`{{execute}}

`curl -X GET http://api.cde:8080/api/guid`{{execute}}

`exit`{{execute}}