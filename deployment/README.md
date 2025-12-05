Once the pod is up - Access the POD
```
kubectl exec -it <POD NAME> -- sh
```

Run the following command
```
curl localhost
```

To test the pod connectiviy from out side of the pod
curl to a Pod IP can fail for several reasons, primarily due to networking scope, port configuration, or the curl command not being installed. The Pod IP is internal to the Kubernetes cluster and not directly accessible from outside by default.

So we have to access the application usting service
Use ```kubectl get services``` to find the external IP and port of your service.
```curl http://<external-ip>:<port>```

Get the external ip of the worker node
```
kubectl get nodes -o wide
```

get the nodeport from service
```
kubectl get svc
```

make a curl call
```
142.93.84.107:32544
```

