Kubernetes has a UI that can be used to visualize the state of the cluster, similar to Kubectl.

Like with the DNS service, the UI also runs inside the cluster.

`
kubectl create -f ~/tutorial/dashboard.yaml
`{{execute}}

After a few moments you will be able to visit the UI on port 8080 with the URL https://[[HOST_SUBDOMAIN]]-8080-[[KATACODA_HOST]].environments.katacoda.com/api/v1/proxy/namespaces/kube-system/services/kubernetes-dashboard

Obs: Usually, https://[[HOST_SUBDOMAIN]]-8080-[[KATACODA_HOST]].environments.katacoda.com/ui should be enough.
