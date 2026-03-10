Auto scaling of Pods Based on Memory Utilization
memory-hpa.yaml in Application Helm chart

apiVersion: autoscaling/v2beta1
kind: HorizontalPodAutoscaler
metadata:
 name: petclinic-memory-hpa
spec:
 maxReplicas: 5
 minReplicas: 1
 scaleTargetRef:
   apiVersion: extensions/v1beta1
   kind: Deployment
   name: petclinic-deployment
 metrics:
 - type: Resource
   resource:
     name: memory
     targetAverageUtilization: 50

Install stress package inside the Application pod

apt-get update
apt-get install stress

Execute stress command to increase memory utilization on pod

stress --vm 1 --vm-bytes 250M  
