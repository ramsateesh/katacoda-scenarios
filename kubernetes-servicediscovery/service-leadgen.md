Let's create leadgen service

![CDE](./assets/leadgen.png)

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

## Logs

Let's monitor the logs for leadgen is a new terminal

`kubectl logs -f -n leadgen -l component=app --all-containers=true`{{execute T3}}