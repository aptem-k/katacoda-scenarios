In this step we will deploy and maintain life cycle of the application.

## Task

Install the chart

`helm install lets-chat --name demo`{{execute}}

List releases

`helm list`{{execute}}

Check deployment status

`helm status demo`{{execute}}

`kubectl get pods`{{execute}}

Upgrade applicattion

`sed -i 's/0.4.6/0.4.7/g' lets-chat/Chart.yaml`{{execute}}

`helm upgrade demo lets-chat --set replicas=2`{{execute}}

Rollback

`helm history demo`{{execute}}

`helm rollback demo 1`{{execute}}

Open application (with node port)

`helm status demo`{{execute}}

http://[[HOST_SUBDOMAIN]]-[[KATACODA_HOST]].environments.katacoda.com

Clean up

`helm delete --purge demo`{{execute}}

`kubectl get pods,deployments,services,replicasets,secrets,configmaps`{{execute}}
