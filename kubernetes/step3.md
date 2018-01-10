In this step we will create config map.

## Task

View settings file

`cat settings.yml`{{execute}}

Create config map using command line tool

`kubectl create configmap mongo-settings --from-file settings.yml`{{execute}}

View config map

`kubectl get configmap mongo-settings -o yaml`{{execute}}
