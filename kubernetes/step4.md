In this step we will deploy frontend.

## Task

View application deployment manifest

`cat lets-chat-app.yml`{{execute}}

Create deployment based on manifest

`kubectl create -f lets-chat-app.yml`{{execute}}

View settings file on pod

`kubectl exec $(kubectl get pods --selector=app=lets-chat,tier=frontend --output=jsonpath={.items..metadata.name}) -it -- bash`{{execute}}

`cat /usr/src/app/config/settings.yml`{{execute}}

`exit`{{execute}}

Display services

`kubectl get services`{{execute}}

Scale the application

`kubectl scale deployment lets-chat-app --replicas=2`{{execute}}

Display pods

`kubectl get pods`{{execute}}

Once all pods are up, open the application using URL below with node port

http://[[HOST_SUBDOMAIN]]-[[KATACODA_HOST]].environments.katacoda.com/
