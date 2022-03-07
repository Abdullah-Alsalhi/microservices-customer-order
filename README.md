# microservices-customer-order

## practincing project for communciation internally through clusterIP between pods.


```bash
kubectl apply -f customer-deployment.yaml
kubectl apply -f order-deployment.yaml
```

```bash
# used port-forwarding for testing the connection 
kubectl port-forward deployment/customer 8080:8080
```

#### This request will go through customer pods to fetch the data from order pods.
```bash
# endpoint to test
http://localhost:8080/api/v1/customer/:id/orders
```