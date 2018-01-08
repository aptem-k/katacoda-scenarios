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

Open the application (once all pods are running)

http://[[CLIENT_SUBDOMAIN]]-8080-[[KATACODA_HOST]].environments.katacoda.com/
