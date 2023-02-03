## Notes
> update ~/.kube/config for given cluster name
> 
> `aws eks update-kubeconfig --name ${cluster_name}`

> Command will create a POD called load-generator at the cluster using the busybox image and would provide us with a bash terminal from the POD container.
> 
> `kubectl run -i --tty load-generator --image=busybox /bin/sh`
>
> Do a `curl` or something more fun from the created pod.


> Start [kubernetes cluster proxy](https://kubernetes.io/docs/tasks/extend-kubernetes/http-proxy-access-api/)
> 
> `kubectl proxy --port=8080`
> 
> When the proxy server is running, we can interact with the cluster API `curl http://localhost:8080/api/v1/namespaces/default/pods`

