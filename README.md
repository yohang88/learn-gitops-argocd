# Learn Gitops with Argo CD

![image](https://user-images.githubusercontent.com/618412/147398226-809d9a07-ee70-4080-836f-55731d32c679.png)

## How To

### Install Argo CD
```
$ cd 01-install-argocd

$ kubectl create namespace argocd

$ kubectl apply -n argocd -f install.yaml
```

### Install Traefik Ingress Controller
```
$ cd 02-install-traefik

$ kubectl create namespace traefik

$ helm install --namespace=traefik --values=values.yaml traefik traefik/traefik
```

### Configure Traefik Routing (ArgoCD, Traefik Dashboard, Traefik Metrics)
```
$ cd 03-install-traefik-routing

$ helm install --namespace=traefik --values=values-production.yaml traefik-routing-helm .
```