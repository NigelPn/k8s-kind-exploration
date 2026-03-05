# Kind commands

Start server with config
```bash
kind create cluster --config simple-nginx-cluster.yml
```

Check nodes running
```bash
kubectl get nodes
```

Start nginx pod (only one pod)
```bash
kubectl apply -f nginx-deployment.yml
```

Check pod running
```bash
kubectl get pods -o wide 
```

Enable Portforwarding for now and curl to check nginx running
```bash
kubectl port-forward $PODNAME 8085:80
curl http://localhost:8085
```

Delete Cluster
```bash
kind delete clusters simple-nginx
```