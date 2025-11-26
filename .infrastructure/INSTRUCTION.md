# How to apply manifests and test the Todo app

## 1. Create namespace, pods and services

```bash
# from repository root
kubectl apply -f _infrastructure/namespace.yml
kubectl apply -f _infrastructure/todoapp-pod.yml
kubectl apply -f _infrastructure/busybox.yml
kubectl apply -f _infrastructure/todoapp-clusterip.yml
kubectl apply -f _infrastructure/todoapp-nodeport.yml

# check resources
kubectl get pods -n todoapp
kubectl get svc  -n todoapp
