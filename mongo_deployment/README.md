# Kubernetes Mongo Deployment

To start with kubernetes and deploy mongodb cluster 

1. First, we have to create the cluster using $minikube$
```bash
    minikube start 
```
the command will start a local cluster and now we have to start deployment 
For checking the cluster is running fine or not 
```
kubectl get all 
```

For getting complete details about the cluster 
```
kubectl describe all
```

2. Now, we have to deploy 
    i. mongo-secrets
    ii. config_map
    iii. mongo_db_deployment
    iv. mongo_express
