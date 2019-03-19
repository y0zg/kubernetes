First Application

Within this directory are the files used to deploy the first application.

Build application.

```console
minikube `docker-env`
docker build -t first-app:v1 .
```

Test application with _Docker_.

```console
docker run -d -p 8000:80 first-app:v1
curl `minikube ip`:8000
```

Test application with _Minikube_.

```console
kubectl -n default apply -f kubernetes
curl `minikube service -n default first-app --url`
```

Deploy kubernetes application
```console
k create -f kubernetes/
```
