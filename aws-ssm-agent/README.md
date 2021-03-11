## Deploying SSM Agent on EKS Cluster

To deploy the SSM DaemonSet configuration on the Amazon EKS cluster, use the following command:

```
kubectl apply -f https://raw.githubusercontent.com/prakarsh-dt/k8s-utilities/main/aws-ssm-agent/ssm-agent-daemonset.yaml && sleep 1 && kubectl delete -f https://raw.githubusercontent.com/prakarsh-dt/k8s-utilities/main/aws-ssm-agent/ssm-agent-daemonset.yaml
```
This command first creates a DaemonSet to run the pods on worker nodes to install SSM Agent, waits for a minute, and then deletes the DaemonSet. 
