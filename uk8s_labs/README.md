```
k apply -f first_pod.yml 
k apply -f webapp-service_nodeport.yml
curl `minikube ip`:30080
# 80 POD port, 8000 exposed localhost port
kubectl port-forward webapp 8000:80
```
