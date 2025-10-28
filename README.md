# GitOps Configuration Repository

This repository contains GitOps configurations for multiple clusters managed by ArgoCD.

## Structure

- `clusters/` - Cluster-specific configurations and ArgoCD Applications
- `apps/` - Application manifests organized by app name
  - `base/` - Base configurations
  - `overlays/` - Environment/cluster-specific overlays

## Clusters

- **okd-1** - Primary OKD cluster

## Applications

- **mce** - Multicluster Engine for Kubernetes

## Deploying Applications

Applications are automatically synced by ArgoCD when changes are pushed to this repository.

To manually deploy the ArgoCD Application definitions:
```bash
oc apply -f clusters/okd-1/argocd-apps/
```
