# ...

## Install configuration

```
kustomize build argocd/env_<infra|...> | k create -f -
```


## Secrets

KubeSeal: https://github.com/bitnami-labs/sealed-secrets

```
kubectl create secret generic myname --from-file sshkey=argocd/base/id_rsa --dry-run -o yaml | kubeseal --format yaml
```
