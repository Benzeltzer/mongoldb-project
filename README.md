# mongoldb-project

►  Deploying MongoDB and Mongo Express

►  MongoDB Pod

►  Secret

►  MongoDB Internal Service

►  Deployment Service and Config Map

►  Mongo Express External Service

I deployed 2 applications mongodb and mongo express.

# 1) start the minikube
```minikube start``` 

# 2) apply the mongo-secret.yaml
```kubectl apply -f mongo-secret.yaml```

# 3) apply the mongo.yaml
```kubectl apply -f mongo.yaml```

# 4) apply the mongo-configmap.yaml
```kubectl apply -f mongo-configmap.yaml```

# 5) apply the mongo-express.yaml
```kubectl apply -f mongo-express.yaml```

# 6) get external ip adress
``` minikube service mongo-express-service```

And then the browser will open and we will see the external service with the IP and the node port.



