In this section we will see how to create/update/delete/list services.

## Create a Service using yaml

```
kubectl apply -f create-service.yaml
```

## Get list of Service

```
kubectl get deployments -n test-namespace
```

## Show Service

```
kubectl get service/nginx-service -o yaml

kubectl get service/nginx-service -o json
```

## Update Service

```
kubectl apply -f update-service.yaml
```

## Delete Service

```
kubectl delete -f create-service.yaml
```
