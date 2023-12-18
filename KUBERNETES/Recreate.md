apiVersion: apps/v1
kind: Deployment
metadata:
  name: myapp-deployment
  labels:
    app: my-app
    type: frontend
spec:
  selector:
    matchLabels:
      app: my-app
  replicas: 10
  strategy:
    type: Recreate 
  minReadySeconds: 10
  revisionHistoryLimit: 3
  template:
    metadata:
      name: my-pod
      labels:
        app: my-app
        type: frontend
    spec:
      containers:
        - name: nginx-container
          image: nginx:1.14.2
