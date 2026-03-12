# Monitoring Setup - Prometheus + Grafana

## Tools Used
- Helm v4.1.1
- Prometheus Community Stack
- Grafana v13.41

## Setup Commands
helm repo add prometheus-community https://prometheus-community.github.io/helm-charts
helm repo update
helm install monitoring prometheus-community/kube-prometheus-stack
kubectl port-forward deployment/monitoring-grafana 3000

## Access
- Grafana URL: http://localhost:3000
- Username: admin

## Dashboard
- Kubernetes / Compute Resources / Cluster
- CPU Utilisation: Real-time
- Memory Usage: Real-time
- Pods: Real-time