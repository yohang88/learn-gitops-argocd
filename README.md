# Learn Gitops with Argo CD

![image](https://user-images.githubusercontent.com/618412/147398226-809d9a07-ee70-4080-836f-55731d32c679.png)

## How To

### Install Argo CD
```
kubectl create namespace argocd

kubectl apply -n argocd -f argocd/install.yml
```

### Traefik Ingress Controller
```
kubectl create namespace traefik

helm install --namespace=traefik --values=traefik/helm-values.yml traefik traefik/traefik
```