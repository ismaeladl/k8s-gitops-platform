# 📦 Helm Workloads

This folder contains the **core application Helm chart** monitored by ArgoCD for automated deployment.

- `templates/` → Deployment, Service, HPA and Ingress manifests.
- `values.yaml` → Common default values.
- `values/values-<env>.yaml` → Environment-specific overrides.

⚡ Purpose: Showcase multi-environment Helm templating with production-aware configurations, ready for CD via ArgoCD.
