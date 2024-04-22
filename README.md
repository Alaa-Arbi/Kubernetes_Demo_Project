# Kubernetes_Demo_Project
This is my first demo project using kubernetes.

I created a MongoDB Pod and connected it to a an internal service. 
Second pod is a a MongoExpress Pod which connects to the MongoDB Pod via the internal service and to the browser via an external service. 
The DB URL is stored in a ConfigMap.
The DB Username, DB Password are stored in a Secret.

![alt text](Diagram.png)
