# kubernetes

## creating a cluster with kind

1. create cluster using kind with one master Node and 2 worker nodes.
2. configure master node with ingress enabled.

```
sudo kind create cluster --config ./cluster/cluster.yaml

```