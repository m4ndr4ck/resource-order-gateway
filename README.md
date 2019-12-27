# Resource Order Gateway

Microserviço que atua como um gateway do Swagger agregando as APIs
de todos os microserviços que compõe o Resource Order.

A agregação se torna possível graças ao Kuberntes Ribbon que se comunica com a API do Kubernetes
para descobrir a localização de cada microserviço.

![Swagger](https://github.com/m4ndr4ck/resource-order-gateway/blob/master/src/main/resources/swagger.png?raw=true)


```
mvn clean package
```

```
docker build . -t oss/resource-order-gateway:1.0 
```

```
kubectl apply -f k8s/deployment.yaml 
```

Acesse por http://services.oss.redecorp/resource-order-gateway/swagger-ui.html
