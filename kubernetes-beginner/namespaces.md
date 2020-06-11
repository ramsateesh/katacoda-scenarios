In this section we will see how to create/update/delete/list namespaces.

## Create a namespace using yaml and cli

```
kubectl apply -f create-namespace.yaml

kubectl create namespace test-namespace2
```

## Get list of namespaces

```
kubectl get namespaces
```

## Show namespace

```
kubectl get namespace test-namespace -o yaml

kubectl get namespace test-namespace2 -o json

kubectl get namespace test-namespace2 --show-labels

kubectl get namespace test-namespace2 -l  network-group=controlled

kubectl get namespace test-namespace2 -l  env=test
```

## Delete namespace

```
kubectl delete -f create-namespace.yaml

kubectl delete ns test-namespace2
```
