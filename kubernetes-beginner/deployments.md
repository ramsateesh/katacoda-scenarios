In this section we will see how to create/update/delete/list deployments.

## Create a Deployment using yaml

```
kubectl create namespace test-namespace

kubectl apply -n test-namespace -f deployment.yaml
```

## Get list of Deployments

```
kubectl get deployments -n test-namespace
```

## Show Deployment

```
kubectl -n test-namespace get deployment/nginx-deploy test-namespace -o yaml

kubectl -n test-namespace get deployment/nginx-deploy test-namespace -o json
```

## Update Deployment

Update replicas in deployment.yaml from 1 to 2.

```
kubectl -n test-namespace apply -f deployment.yaml
```

## Delete Deployment

```
kubectl -n test-namespace delete -f deployment.yaml
```
