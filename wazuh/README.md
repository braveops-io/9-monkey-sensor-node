## Wazuh HIDS Kubernetes


### Run the wazuh HIDs in kubernetest in minishift and EKS


####
Deploy the following componets

0. Base (0-base)
Base setup before deploy into cluster

1. Logstash (1-logstash)

To bridge beats and logs and transfer them into elasticsearch.

2. Wazuh Manager and API (2-wazuh-manager)
 
Runs the OSSEC master and clients endpoint. And the wazuh API to register new clients.
Trigger alerts and then send them to Logstash for forwarding to Elasticsearch.

3. Agent (3-agent)

Runs the agent on every node. Collects node data and send to the manager-workers.
Diffrent configs and deploymenst depending where to deploy and what files to monitor.


4. ELK (00-elk)
Only needed for test to run own ELasticsearch and Kibana



### Alerts 


[agend] -- > [manager-workers] --> [master] --> [Logstash] --> [Elasticsearch]


### Disk

The Wazuh manager and worker nodes need to have disk to work.
In minicube they use local disk and in EKS NFS disk to ba able to move in all zones.


