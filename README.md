# cgr-events-dashboard
Events dashboard for the purpose of tracking customer registry events and metrics

## Generate a GCP authentication key for use by OTEL



## Deploy Open Telemetry with Google Cloud Exporter

```bash
helm repo add open-telemetry https://open-telemetry.github.io/opentelemetry-helm-charts

helm repo update

helm upgrade -i opentelemetry-collector open-telemetry/opentelemetry-collector \
--values helm/otel-values.yaml \
-n opentelemetry-collector \
--create-namespace 
```

## Deploy the grafana k8s monitoring stack

```bash
helm repo add grafana https://grafana.github.io/helm-charts
helm repo update

helm upgrade -i k8s-monitoring grafana/k8s-monitoring \
--create-namespace \
--set cluster.name=cluster1 \
--values helm/k8s-monitoring-values.yaml \
-n k8s-monitoring
```