In this step we will deploy frontend.

## Task

View deployment manifest

`cat lets-chat-app.yml`{{execute}}

Create deployment based on manifest

`kubectl create -f lets-chat-app.yml`{{execute}}

Display services

`kubectl get services`{{execute}}

Scale the application

`kubectl scale --replicas=2 deployment lets-chat-app`{{execute}}

Display pods

`kubectl get pods`{{execute}}

Once all pods are up, open the application using URL below with node port

http://[[HOST_SUBDOMAIN]]-[[KATACODA_HOST]].environments.katacoda.com/
