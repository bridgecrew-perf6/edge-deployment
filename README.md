# edge-deployment
Collector Farm Deployment Manifests


## Architecture






## To send traffic
Collector farm opens a otlp ingestion point `appd-otel-collector:4317`.  

- If using OpenTelemetry Collector collector, following is the exporter  
```yaml
  otlp:
    endpoint: appd-otel-collector:4317
    tls:
      insecure: true
```
