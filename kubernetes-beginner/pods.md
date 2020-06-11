In this section we will see how to create/update/delete/list pods.

## Create a pod using yaml

```
kubectl create namespace test-namespace

kubectl -n test-namespace apply -f create-pod.yaml
```

## Get list of pod

```
kubectl get pods -n test-namespace
```

## Show pod

```
kubectl -n test-namespace get pod/nginx -o yaml

kubectl -n test-namespace get pod/nginx -o json
```

## Delete pod

```
kubectl -n test-namespace delete -f create-pod.yaml
```
