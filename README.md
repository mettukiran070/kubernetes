# kubernetes

## creating a cluster with kind

1. create cluster using kind with one master Node and 2 worker nodes.
2. configure master node with ingress enabled.

```
sudo kind create cluster --config ./cluster/cluster.yaml
```

## kubernetes deployment
1. create a deployment.

```
sudo kubectl apply -f ./deployments/deployment.yaml
```

## kubernetes service
1. create a service for the above deployment.

```
sudo kubectl apply -f ./services/service.yaml
```

2. If we create a service using NodePort type then it can be accessed by using node ip

```
sudo kubectl get nodes -o wide
```

take internal ip from above command response and access it in your local.

3. To Access service in local, need to port-forward the service.

```
sudo kubectl port-forward svc/spring-service 8080:8080
```

## Ingress
