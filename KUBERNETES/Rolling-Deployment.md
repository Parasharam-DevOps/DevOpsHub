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
  replicas: 6
  strategy:
    type: RollingUpdate
    rollingUpdate:
      maxSurge: 2
      maxUnavailable: 2
  minReadySeconds: 5
  revisionHistoryLimit: 2
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


          
