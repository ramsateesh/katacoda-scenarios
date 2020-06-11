In this section we will see how to create/update/delete/list pods.

## Create a pod using yaml

```
kubectl apply -f create-pod.yaml
```

## Get list of pod

```
kubectl get pods -n test-namespace
```

## Show pod

```
kubectl get pod/nginx test-namespace -o yaml

kubectl get pod/nginx test-namespace -o json
```

## Delete pod

```
kubectl delete -f create-pod.yaml
```
