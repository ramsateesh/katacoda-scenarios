Let's recap what we learned in the previous session.

### Namespace
We created a namespace in which we can work.

`kubectl apply -f namespace.yaml`{{execute}}

`kubectl get namespaces`{{execute}}

### Static Pod
We created a static pod with the below command.

`kubectl apply -f static-pod.yaml`{{execute}}
`kubectl -n test-namespace get pods`{{execute}}

### Service
We created a service for our static-pod with the below command.

`kubectl apply -f service.yaml`{{execute}}
`kubectl -n test-namespace get svc`{{execute}}

### Cleanup Static-Pod and Service

`kubectl -n test-namespace delete -l app=nginx `{{execute}}

### Deployment
We created a deployment with the below command.

Creating nginx Deployment

`kubectl apply -f deployment.yaml`{{execute}}

Creating nginx Service

`kubectl apply -f service.yaml`{{execute}}

See what has been created

`kubectl -n test-namespace get all`{{execute}}

### Cleanup

Let's clean up before we move on to service discovery

`kubectl -n test-namespace delete -l app=nginx `{{execute}}

`kubectl delete namespace test-namespace`{{execute}}