In this step we will verify the cluster is up and running.

## Task

Print the client and server versions for the current context

`kubectl version`{{execute}}

Display running kubernetes services

`kubectl cluster-info`{{execute}}

Display system pods

`kubectl get pods -n kube-system`{{execute}}
