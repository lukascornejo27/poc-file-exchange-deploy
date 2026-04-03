# poc-file-exchange-deploy

Repositorio de despliegue GitOps para la PoC de intercambio de archivos en AWS.

## Estructura

- `k8s/`: manifiestos Kubernetes de la aplicación
- `argocd/`: definición de Application de Argo CD

## Flujo

1. Se actualizan manifiestos en este repo
2. Se realiza push a `main`
3. Argo CD detecta cambios
4. Argo CD sincroniza con EKS
5. Kubernetes aplica el estado deseado