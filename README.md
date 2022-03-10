# edge-deployment
Collector Farm Deployment Manifest

## Architecture



## Installation

The deployment is meant to work with [OpenTelemetry Operator][https://github.com/open-telemetry/opentelemetry-operator]. 

### Pre-requisites 

- Install OpenTelemetry Operator using these instructions [https://github.com/open-telemetry/opentelemetry-operator#getting-started]


```bash

$ kubectl apply -f https://github.com/cert-manager/cert-manager/releases/download/v1.7.1/cert-manager.yaml

$ kubectl apply -f https://github.com/open-telemetry/opentelemetry-operator/releases/latest/download/opentelemetry-operator.yaml

```

### Install the collector farm

```bash
 kubectl apply -f collector-farm.yaml
```


## To send traffic
Collector farm opens a otlp ingestion point `appd-otel-collector:4317`.  

- If using OpenTelemetry Collector collector, following is the exporter  
```yaml
  otlp:
    endpoint: appd-otel-collector:4317
    tls:
      insecure: true
```
