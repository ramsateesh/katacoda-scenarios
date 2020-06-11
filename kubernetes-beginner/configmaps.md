In this section we will see how to create/update/delete/list ConfigMap also to inject a ConfigMap into a Pod.

## Create a ConfigMap using yaml

```
kubectl apply -f create-service.yaml
```

## Get list of ConfigMap

```
kubectl get deployments -n test-namespace
```

## Show ConfigMap

```
kubectl get service/nginx-service test-namespace -o yaml

kubectl get service/nginx-service test-namespace -o json
```

## Delete ConfigMap

```
kubectl delete -f create-service.yaml
```

## Inject a ConfigMap into a pod as a file

```
kubectl apply -f pod-configmap-file.yaml
```