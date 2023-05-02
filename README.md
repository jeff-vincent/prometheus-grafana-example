# Prometheus-Example

Run the following command to deploy Prometheus and Grafana. 
```
helm repo add prometheus-community https://prometheus-community.github.io/helm-charts
helm repo add grafana https://grafana.github.io/helm-charts
```

```
helm dependency build
```

```
helm template . -f values.yaml --name-template=velocity | kubectl apply -f -
```

