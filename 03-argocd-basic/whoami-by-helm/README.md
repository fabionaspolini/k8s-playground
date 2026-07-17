```bash
argocd app create whoami-v2-by-helm \
  --repo https://github.com/fabionaspolini/k8s-playground \
  --path helm-charts/whoami \
  --dest-server https://kubernetes.default.svc \
  --dest-namespace teste-argocd-v2 \
  --values "../../03-argo-cd-basic/whoami-by-helm/custom-values.yaml"

  --values "values.yaml"
  --values "03-argo-cd-basic/whoami-by-helm/custom-values.yaml"

argocd app delete whoami-v2-by-helm -y
```