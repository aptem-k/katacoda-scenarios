In this step we will deploy the chart.

## Task

Install the chart

`helm install lets-chat --name demo`{{execute}}

List releases

`helm list`{{execute}}

Check deployment status

`helm status demo`{{execute}}

`kubectl get pods`{{execute}}

Upgrade applicattion

sed -i 's/0.4.6/0.4.7/g' lets-chat/Chart.yaml

`helm upgrade demo lets-chat --set replicas=2`{{execute}}

Rollback

`helm rollback demo 1`{{execute}}
