# bootstrap a kubernetes cluster 

```
kind create cluster --config=kind-config.yaml
```

# Deploy kubestate metrics 

```
cd kube-state-metrics &&  kubectl -n kube-system apply -f .
```
```
kubectl get pods -n kube-system
```

# Deploy prometheus 

```
k create ns monitoring
```

```
cd prometheus  &&   kubectl -n monitoring apply -f .
```

```
kubectl get pods -n monitoring
```