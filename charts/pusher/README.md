# Helm Chart - Pyth Price Pusher
this helm chart deploys the full stack components required to push cryptocurrency prices to the Pyth network. The chart supports setting up multiple chains with customized price configurations for each individual chain.

# Usage
```
helm repo add https://charts.keom.io
helm upgrade --install pyth-pusher keom/pyth-pusher --namespace pyth --create-namespace --values values.yml
```

# Notes
The resource allocations is relaxed to ensure smooth operations. Might improve in future versions

# TODO
- Move resource assignment to values.yml
- Add monitoring stack to monitor gas prices and expenses
- Alerts when pusher wallets passes a preset threshold
- Ingress option to expose price-service for dapps
