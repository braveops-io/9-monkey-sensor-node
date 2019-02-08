# Wazuh manager master StatefulSet and base services

This will deploy the logstash server.

It will open the port 5000 as a beats service and send log into elasticsearch 



## Deploy
```BASH
kubectl apply -f logstash-deploy-config.yaml  
kubectl apply -f logstash-deploy.yaml  
kubectl apply -f logstash-svc.yaml
```