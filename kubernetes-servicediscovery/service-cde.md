Let's create cde service

Below command creates following:

* Namespace (cde)
* Deployment (api-guid-generator)
* Service (api-guid-svc)
* Static pod (explorer)

`kubectl apply -f service-cde.yaml`{{execute}}

See what got created

`kubectl -n cde get all`{{execute}}