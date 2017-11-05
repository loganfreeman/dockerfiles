```
minikube start --vm-driver=xhyve
kubectl config use-context minikube
kubectl cluster-info
eval $(minikube docker-env)
docker build -t hello-node:v1 .
kubectl run hello-node --image=hello-node:v1 --port=8080
kubectl get deployments
kubectl get pods
kubectl expose deployment hello-node --type=LoadBalancer
kubectl get services
minikube service hello-node
kubectl delete service hello-node
kubectl delete deployment hello-node
minikube stop
eval $(minikube docker-env -u)
```
