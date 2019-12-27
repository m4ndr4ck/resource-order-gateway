# Resource Order Gateway

Microserviço que atua como um gateway do Swagger agregando as APIs
de todos os microserviços que compõe o Resource Order.

A agregação se torna possível graças ao Kuberntes Ribbon que se comunica com a API do Kubernetes
para descobrir a localização de cada microserviço. 


```
mvn clean package
```

```
docker build . -t oss/resource-order-gateway:1.0 
```

```
kubectl apply -f k8s/deployment.yaml 
```
