# api-produto

## Docker Build

```cli
docker build -t flpinheiro/api-k8s-bootcamp-produto:v1 -f .\src\Dockerfile .\src
```

## Docker Tag

```cli
docker tag flpinheiro/api-k8s-bootcamp-produto:v1 flpinheiro/api-k8s-bootcamp-produto:latest
```

## docker push

```cli
docker push flpinheiro/api-k8s-bootcamp-produto:v1
docker push flpinheiro/api-k8s-bootcamp-produto:latest
```

## k3d install

```cli
choco install k3d
```

## create cluster

```cli
k3d cluster create mycluster --agents 3 --servers 3 -p 8080:30000@loadbalancer
```

## delete cluster

```cli
k3d cluster delete mycluster
```

## kubctl apply

```cli
kubectl apply -f .\k8s\mongodb\deployment.yml
kubectl apply -f .\k8s\mongodb\service.yml
kubectl apply -f .\k8s\api\deployment.yml
kubectl apply -f .\k8s\api\service.yml
kubectl apply -f .\k8s\ -R
```

## kubectl get

```cli
kubectl get pods
kubectl get services
kubectl get all
```

## kubectl top pods

```cli
kubctl top pods
```

[metric server](https://github.com/kubernetes-sigs/metrics-server)

## horizontal pod auto scale

escalar a aplicação sempre que o pod atingir alguma metrica de request, por exemplo sempre que o pod atingir 80% de cpu.
