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
kubectl apply -f nginx-pod.yaml
```

Check pod running
```bash
kubectl get pods -o wide 
```

Enable Portforwarding for now and curl to check nginx running
```bash
kubectl port-forward pod/nginx 8085:80
curl http://localhost:8080
```

Start server with config
```bash
kind delete clusters simple-nginx

```