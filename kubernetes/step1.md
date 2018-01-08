In this step we will prepare Helm tool.

## Task

Download Helm

`curl -LO https://storage.googleapis.com/kubernetes-helm/helm-v2.7.2-linux-amd64.tar.gz;tar -xvf helm-v2.7.2-linux-amd64.tar.gz;mv linux-amd64/helm /usr/local/bin/`{{execute}}

Initialize

`helm init`{{execute}}

Update respository

`helm repo update`{{execute}}

Check all system services are up

`kubectl get pod -n kube-system`{{execute}}
