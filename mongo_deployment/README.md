# Kubernetes Mongo Deployment

To start with kubernetes and deploy mongodb cluster 
For this deployment, we are using mongodb and mongo-express for interactions 

Deployment process
1. Add the secret credentials in the cluster
``` 
kubectl apply -f mongo_config_map.yaml
```
For checking if it successfully applied 
```
kubectl get secrets

or 

kubectl describe secrets
```

2. Deploy the MongoDB and start the DB service 

```
kubectl apply -f mongo-deployment.yaml
```

For checking 
```
kubectl get pods

or 

kubectl get pod mongo-db-xxxx --watch
```

To get the logs 
```
kubectl logs mongo-db-xxxxx 
```

3. Add Configuration Map
```
kubectl apply -f mongo_config_map.yaml
```

4. Add Mongo-express for interactions

```
kubectl apply -f mongo-express.yaml
```

5. Exposing the service 
```
minikube service mongodb-express
```