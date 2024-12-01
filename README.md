# argocd-apps
Applications to use in ArgoCD

# Install

* Deploy ArgoCD using Kustomize

```
kubectl config current-context

kubectl create namespace argocd

kubectl apply -k ./init
```

* Deploy app-of-apps

```
kubectl apply -f ./app-of-apps.yaml
```

* Update DNS
