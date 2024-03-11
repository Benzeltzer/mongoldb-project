# mongoldb-project

►  Deploying MongoDB and Mongo Express

►  MongoDB Pod

►  Secret

►  MongoDB Internal Service

►  Deployment Service and Config Map

►  Mongo Express External Service

I deployed 2 applications mongodb and mongo express.
when i created mongo express deployment i needed two things: 
1) database URL of mongodb so that mongo express can connect to it.
2) credentials, so the way we can pass this sensetive infromation to mongo express its throgh his deployment configuration file throgh environmental variabels that i looked in docker, because that how the application is configured.
 
so, i created config map that contains data base URL, and create a secret that contains the credentials and put both in same deployment file.





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



