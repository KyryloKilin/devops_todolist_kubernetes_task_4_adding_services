# How to apply manifests and test the Todo app

## 1. Create namespace, pods and services

```bash
# from repository root
kubectl apply -f .infrastructure/namespace.yml
kubectl apply -f .infrastructure/todoapp-pod.yml
kubectl apply -f .infrastructure/busybox.yml
kubectl apply -f .infrastructure/todoapp-clusterip.yml
kubectl apply -f .infrastructure/todoapp-nodeport.yml

# check resources
kubectl get pods -n todoapp
kubectl get svc  -n todoapp

# Example of lunch with port-forward
kubectl port-forward service/kube2py-service 8081:80

# Example of creation of the NodePort service
kubectl apply -f nodeport.yml
kubectl get svc 