# Scenario 02-helm

```bash
helm upgrade --install 02-helm ./helm-charts/whoami --namespace teste -f ./02-helm/values-prod.yaml

helm uninstall --namespace teste 02-helm
```