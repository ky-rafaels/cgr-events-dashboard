# cgr-events-dashboard
Events dashboard for the purpose of tracking customer registry events and metrics

## Deploy Open Telemetry with Google Cloud Exporter

```bash
helm repo add open-telemetry https://open-telemetry.github.io/opentelemetry-helm-charts

helm repo update

helm upgrade -i opentelemetry-collector open-telemetry/opentelemetry-collector \
--values helm/otel-values.yaml \
-n opentelemetry-collector \
--create-namespace 
```