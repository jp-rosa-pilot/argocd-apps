
### argocd application

```yaml
apiVersion: argoproj.io/v1alpha1
kind: Application
metadata:
  name: springboot-poc-mutu
spec:
  destination:
    name: ''
    namespace: devteam
    server: 'https://kubernetes.default.svc'
  source:
    repoURL: 'https://github.com/jp-rosa-pilot/argocd-apps.git'
    path: springboot-poc-mutu/overlays/uat
    targetRevision: HEAD
  sources: []
  project: default
  syncPolicy:
    automated: {}
```
