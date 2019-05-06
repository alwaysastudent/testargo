# ArgoCD configuration

## Structure

* `base/base`: contains original argocd resources.
* `base/app`: contains reference to argocd for self-management


## Update ArgoCD base

The base in `base/base` can be updated by editing the version tag in `base/base/source/kustomization.yaml` and running
```
kustomize build base/base/source > base/base/argocd.yaml
```

and committing the result.
