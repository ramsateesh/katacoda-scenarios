Let's explore service discovery

![CDE](./assets/nodeport-services.png)

## Expose the API (cde) on NodePort

`kubectl -n cde apply -f nodeport-api-service.yaml`{{execute}}

`ip -f inet a | grep "global ens3" | awk '{print $2}'| sed "s/\/16//g"`{{execute}}

`HOST_IP=`{{copy}}

`CDE_NP=30081`{{execute}}

`curl -X http://$HOST_IP:$CDE_NP/api/guid`{{execute}}

## Expose the APP (leadgen) on NodePort

`kubectl -n leadgen apply -f nodeport-app-service.yaml`{{execute}}

`LEADGEN_NP=30081`{{execute}}

`curl -X http://$HOST_IP:$LEADGEN_NP/api/guid`{{execute}}