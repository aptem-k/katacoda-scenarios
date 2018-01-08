In this step we will deploy frontend.

## Task

View deployment manifest

`cat lets-chat-app.yml`{{execute}}

Create deployment based on manifest

`kubectl create -f lets-chat-app.yml`{{execute}}

Print services

`kubectl get services`{{execute}}

Print pods

`kubectl get pods`{{execute}}

Once all pods are up, open the application using URL below with node port

http://[[MASTER_SUBDOMAIN]]-[[KATACODA_HOST]].environments.katacoda.com/
