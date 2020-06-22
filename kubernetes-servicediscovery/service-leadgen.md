Let's create leadgen service

Below command creates following:

* Namespace (leadgen)
* Deployment (api-guid-generator)
* Service (api-guid-svc)
* Static pod (explorer)

`kubectl apply -f service-leadgen.yaml`{{execute}}

See what got created

`kubectl -n leadgen get all`{{execute}}