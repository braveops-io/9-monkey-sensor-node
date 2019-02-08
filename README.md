# 9-monkey-sensor-node


## Node sensor 

Here we are adding diffrent types of sensor that w ecan run on the nodes.

The sensor are to protect the kubernetes node in runtime and to alert.

## All logs and alerts are sen on to Highground (Our ELK stack)

We use the sensors to pick up data and then pass it along to our Highground and ELK stack. There we can vizulize and trigger alerts on the data.


### Wazuh
Wazuh is our base node HIDS setup. It will deploy a wazuh master and workers on the cluster.
Then it deploy agenst as deamonset to pick up logs from the nodes and pass them on to the workers and onto the Highground setup


