In this step we will explore Kubernetes dashboard.

## Task

Deploy the dashboard

`kubectl apply -f https://raw.githubusercontent.com/kubernetes/dashboard/master/src/deploy/recommended/kubernetes-dashboard.yaml`{{execute}}

Check pod status

`kubectl get pods -n kube-system -l k8s-app=kubernetes-dashboard`{{execute}}

Once all pod is up, start proxy

`kubectl proxy --address='0.0.0.0' --port=8080 --accept-hosts='^*$'&`{{execute}}

Open the application using URL below

http://[[HOST_SUBDOMAIN]]-8080-[[KATACODA_HOST]].environments.katacoda.com/api/v1/namespaces/kube-system/services/https:kubernetes-dashboard:/proxy/

Use Ctrl+C to stop the proxy

Clean up

`kubectl delete pods,deployments,services,secrets --all`{{execute}}

`kubectl get pods,deployments,services,replicasets,secrets`{{execute}}
