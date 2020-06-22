Let's recap what we learned in the previous session.

### Namespace
We created a namespace in which we can work.

`kubectl apply -f namespace.yaml`{{execute}}

`kubectl get namespaces`{{execute}}

### Static Pod
We created a static pod with the below command.

`kubectl apply -f static-pod.yaml`{{execute}}

### Service
We created a service for our static-pod with the below command.

`kubectl apply -f service.yaml`{{execute}}