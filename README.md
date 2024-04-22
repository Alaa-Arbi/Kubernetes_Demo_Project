# Kubernetes_Demo_Project
This is my first demo project using kubernetes.

I created a MongoDB Pod and connected it to a an internal service. 
Second pod is a a MongoExpress Pod which connects to the MongoDB Pod via the internal service and to the browser via an external service. 
The DB URL is stored in a ConfigMap.
The DB Username, DB Password are stored in a Secret.

![alt text](Diagram.png)


First creat the cluster 
'''bash
minikube start 
''' 
Start by creating the secret to store the database credentials:
'''bash 
kubectl apply -f mongo-secret.yaml
'''
Now we create the MongoDB Pod and its service and reference the secret inside it to get the credentials
'''bash 
kubectl apply -f mongoDB.yaml
'''
Then we create the config map that will store the database url which is nothing else but the service attached to the monogoDB database. 
'''bash 
kubectl apply -f mongo-configmap.yaml
'''
