```bash
argocd app create -f root-app.yml

argocd app sync root-app

# sync all
argocd app list -o name | xargs -I {} argocd app sync {}

argocd app delete root-app -y
```