In this section we will see how to create/update/delete/list deployments.

## Create a Deployment using yaml

```
kubectl apply -f create-deployment.yaml
```

## Get list of Deployments

```
kubectl get deployments -n test-namespace
```

## Show Deployment

```
kubectl get deployment/nginx-deploy test-namespace -o yaml

kubectl get deployment/nginx-deploy test-namespace -o json
```

## Update Deployment

```
kubectl apply -f update-deployment.yaml
```

## Delete Deployment

```
kubectl delete -f create-deployment.yaml
```
