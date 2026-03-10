Metric server is required for Horizontal Pod Autoscaler
What is Metric Server?

It collects metrics like CPU, memory or Disk IO consumption for containers or nodes, from the Summary API, exposed by Kubelet on each node.

Enable 4443 port on Master and Worker Nodes

4443

Clone Metric-server helm chart on K8 Master

git clone https://github.com/prawinkorvi/metric-server.git

Create Metric Server

kubectl create -f .
kubectl top pods
kubectl top nodes
