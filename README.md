# Argo CD Configs

## Configuring this repo on a new argo instance

1. Login to Argo CD
2. Settings > Connect Repo > git > repo url
3. Add new application
4. Use existing repo url
5. path (ex: excalidraw)
6. cluster default
7. use argo config repo
8. save settings
9. sync > synchronize
10. validate app is green after syncing

## Accessing Argo login password

```bash
kubectl --namespace argocd get secret argocd-initial-admin-secret -o json | jq -r '.data.password' | base64 -d
```
