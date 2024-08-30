# Alguns comandos executados no Day01

kind create cluster --config kind-cluster.yaml --name giropops

kind delete cluster

kubectl get pods -n kube-system

kubectl get deployment -A

kubectl get service -A (-A: ver em todos os namespaces)

kubectl run --image nginx --port 80 giropops

kubectl exec -ti giropops -- bash

kubectl exec -ti giropops -- ls /proc

kubectl expose pods giropops --type NodePort

kubectl run --image nginx --port 80 giropops --dry-run=client -o yaml

kubectl run --image nginx --port 80 giropops --dry-run=client -o yaml > pod.yaml

kubectl apply -f pod.yaml