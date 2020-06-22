Let's recap what we learned in the previous session.

### Namespace
We created a namespace in which we can work.

<pre>
kubectl apply -f namespace.yaml {{execute HOST1}}

kubectl get namespaces {{execute HOST1}}
</pre>

### Static Pod
We created a static pod with the below command.

<pre>
kubectl apply -f static-pod.yaml {{execute HOST1}}
</pre>

### Service
We created a service for our static-pod with the below command.

<pre>
kubectl apply -f service.yaml {{execute HOST1}}
</pre>