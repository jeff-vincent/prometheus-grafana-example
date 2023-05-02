# Prometheus-Example

Run the following command to deploy an instance of Prometheus and Grafana that is configured to scrape metrics from [`fastapi-mongo-video`](https://github.com/jeff-vincent/fastapi-mongo-video)
```
helm repo add prometheus-community https://prometheus-community.github.io/helm-charts
helm repo add grafana https://grafana.github.io/helm-charts
```

```
helm dependency build
```

```
kubectl create ns monitoring
```

```
helm template . -f values.yaml --name-template=velocity --namespace=monitoring | kubectl apply -f - --namespace=monitoring
```

