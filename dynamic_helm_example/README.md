# 🌐 Dynamic Helm Examples

This folder demonstrates a **multi-environment Helm setup using a single shared `values.yaml`**.  

- Includes a sample Ingress template to illustrate environment-specific routing.  
- No per-environment `values` files: all environments are configured dynamically from one file.

## Usage

Environment selection can be achieved in two ways:

- flag **--set env=value** must be called on helm command
- parameters can be passed to ArgoCD template (see **argocd/app** directory)

⚡ Purpose: Show how Helm can adapt to multiple environments with minimal duplication.

## Note
Ingress has been choosen due to simplicity to demonstrate how it change from test to prod when applied