In this step we will deploy database.

## Task

View deployment manifest

`cat lets-chat-mongo.yml`{{execute}}

Create deployment based on manifest

`kubectl create -f lets-chat-mongo.yml`{{execute}}

Display deployments

`kubectl get deployments`{{execute}}

Display pods

`kubectl get pods`{{execute}}

Display services

`kubectl get services`{{execute}}

Monitor pod

`kubectl describe pod -l app=lets-chat,tier=backend`{{execute}}

View log

`kubectl logs -l app=lets-chat,tier=backend`{{execute}}

Login to pod machine

`kubectl exec $(kubectl get pods --selector=app=lets-chat,tier=backend --output=jsonpath={.items..metadata.name}) -it -- bash`{{execute}}

`ls /data/db`{{execute}}

`exit`{{execute}}

