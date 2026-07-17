# k8s-playground

- `helm-charts`: Pacotes reutilizáveis via helm.
- `scenarios`: Cenários de teste para aplicar atualizações no cluster k8s.


## Subir container

```bash
kubectl \
    run fabio-temp-net-utils \
    -i --tty --rm --restart=Never \
    --namespace teste \
    --image=fabionaspolini/net-utils \
    --image-pull-policy=Always \
    -- \
    bash
```

## Helm

```bash
cd helm-charts
helm lint ./whoami

# Syntax
# helm install <release-name> ./<heml-chat-folder>

# Simular execução
helm install teste ./whoami --dry-run

# Realizar deploy
helm install teste ./whoami --namespace teste

# Atualizar deploy
helm upgrade teste ./whoami --namespace teste --set replicaCount=3

# Remover
helm uninstall teste --namespace teste

# Instalar ou atualizar deploy
helm upgrade --install teste ./whoami --namespace teste -f ./whoami/values-prod.yaml
```
