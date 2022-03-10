# edge-deployment
Collector Farm Deployment Manifests


## Architecture






## To send traffic
Collector farm opens a otlp ingestion point `appd-otel-collector:4317`.  

- If using OpenTelemetry Collector, following is the exporter configuration
```yaml
  otlp:
    endpoint: appd-otel-collector:4317
    tls:
      insecure: true
```
