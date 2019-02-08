# Wazuh manager master StatefulSet and base services

This will deploy the wazuh master service.

The master service will run and thensend logs to the logstash service and then on to elasticsearch

## Deploy
```BASH
kubectl apply -f wazuh-api-svc.yaml
kubectl apply -f wazuh-manager-cluster-sts-svc.yaml
kubectl apply -f wazuh-workers-svc.yaml

kubectl apply -f wazuh-manager-master-conf.yaml
kubectl apply -f wazuh-manager-worker-0-conf.yaml
kubectl apply -f wazuh-manager-worker-1-conf.yaml

kubectl apply -f wazuh-manager-master-sts.yaml
kubectl apply -f wazuh-manager-worker-0-sts.yaml
kubectl apply -f wazuh-manager-worker-1-sts.yaml

```
