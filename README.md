# cgr-events-dashboard
Events dashboard for the purpose of tracking customer registry events and metrics

## Deploy Open Telemetry with Google Cloud Exporter

```bash
helm repo add open-telemetry https://open-telemetry.github.io/opentelemetry-helm-charts

helm repo update

helm upgrade -i open-telemetry \
--values ./helm/otel-values \
--create-namespace 
```