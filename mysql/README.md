# Mysql Setup in kubernetes

## steps to create mysql deployment in kubernetes

1. apply above all the yaml files in the otrder of PV, PVC, Deployment and service.

```
    kubectl apply -f ./../
```

2. To connect with the database use below command 

```
    kubectl run -it --rm --image=mysql:8.0 --restart=Never mysql-client -- mysql -h mysql-service --password="mysqlrootpass"
```