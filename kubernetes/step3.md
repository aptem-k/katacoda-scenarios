In this step we will deploy database.

## Task

Create deployment based on manifest

`kubectl create -f lets-chat-mongo.yaml`{{execute}}

Print deployments

`kubectl get deployments`{{execute}}

Print pods

`kubectl get pods`{{execute}}

Print services

`kubectl get services`{{execute}}

Monitor pod

`kubectl describe pod -l app=lets-chat,tier=backend`{{execute}}
