# ArgoCD, used to deploy fundamental K8s apps.

## Initial deployment

First make sure kubectl is connected to your Kubernetes cluster.

```shell
helm repo add argo https://argoproj.github.io/argo-helm
helm repo update
helm upgrade --install --create-namespace -n argocd argocd argo/argo-cd --version 8.3.0
kubectl apply -f argocd-bootstrap.yaml
```
