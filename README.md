# k8s-gitops-platform
# 🚀 DevOps Demo Portfolio

This repository demonstrates a **GitOps workflow** using Helm and ArgoCD, showcasing multi-environment deployments, dynamic templating, and production-aware configurations.

---

## 📂 Repository Structure

- **🟢 `argoCD/`**  
  ArgoCD application manifests and configurations.  
  Watches the **`helm/`** folder for automated deployment in the demo CD pipeline.

- **📦 `helm/`**  
  Core application workloads with Helm templates:  
  - `templates/` → Deployment, Service, HPA and Ingress manifests.  
  - `values.yaml` → Common default values to all environments.  
  - `values/values-<env>.yaml` → Environment-specific overrides.  
  This folder is actively monitored by ArgoCD for deployment.

- **🌐 `dynamic_helm_examples/`**  
  Example of a multi-environment Helm setup using **one shared `values.yaml`**.  
  Includes a sample Ingress template to illustrate environment-specific routing.

- **🛠️ `cluster_config_example/`**  
  Plain Kubernetes manifests (Namespace, Quotas, LimitRanges, NetworkPolicies, PDBs, etc.)  
  Demonstrates how production-grade cluster configuration could support prod workloads in **`helm/`**.

---

## 🎯 Purpose

This repository showcases **practical DevOps expertise**:

- Multi-environment Helm templating with environment-specific values.  
- Continuous Deployment via ArgoCD.  
- Production-aware cluster configuration and workload protection.  
- Demonstration of scaling, probes, resource limits, and security best practices.  

> All examples are fully functional for demonstration purposes in the test environment and illustrate what could be configured in a production-grade deployment scenario.

Note that the prod environment cannot be deployed due to the limited functionality of the image used as application.
