# prometheus
Running Prometheus on Kubernetes AWS, GCP, Azure and On-Premise


Run all the YAML files in the repo to deploy the prometheus application. 

1. Create the monitoring namespace - "kubectl apply  -f namespace.yml"
2. Prometheus should have correct permissions to the Kubernetes API. run "kubectl apply -f clusterRole.yml"
3. ConfigMap to decouple any configuration artifacts from image content. This will help keep containerized applications more portable. "kubectl apply -f config-map.yml"
4. Prometheus Deployment and Service to start the application - "kubectl apply -f prometheus-deployment.yml"

Once the pod and service are available, you can access Prometheus’s Browser by going to http://<KUBERNETES_MASTER_IP>:30000

