In this step we will inspect our chart.

## Task

Update dependencies

`helm dependency update lets-chat`{{execute}}

`ll lets-chat/charts`{{execute}}

Inspect

`helm inspect lets-chat`{{execute}}

Examine a chart for possible issues

`helm lint lets-chat`{{execute}}

Simulate installation

helm install --debug --dry-run lets-chat
