# App-of-Apps

Central repository that holds ArgoCD `Application` manifests. ArgoCD watches the `apps/` directory and automatically deploys everything defined here.

## Layout

```
apps/
├── metallb.yaml          # MetalLB (sync-wave 1)
└── nginx-ingress.yaml    # NGINX Ingress Controller (sync-wave 2)
```

## Adding a new application

Create a new `apps/<name>.yaml` with an ArgoCD `Application` resource pointing to the chart/repo for that component. ArgoCD will pick it up automatically.
