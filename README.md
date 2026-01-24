# ArgoCD ApplicationSet Controller – Multi-Cluster Deployment

This repository demonstrates a **multi-cluster GitOps deployment** using the **ArgoCD ApplicationSet Controller** to deploy and manage applications across multiple Amazon EKS clusters.

The setup uses a **single Git repository** to deploy the Sock Shop microservices application consistently across clusters in different AWS regions.

---

## Architecture Overview

- Two Amazon EKS clusters:
  - Mumbai region
  - US region
- Centralized ArgoCD control plane
- ApplicationSet Controller for multi-cluster automation
- Sock Shop microservices deployed using Kustomize
- Secure inter-cluster communication via VPC peering

---

## Key Features

- Multi-cluster application deployment using ApplicationSet
- Centralized GitOps workflow with ArgoCD
- Dynamic generation of ArgoCD Applications per cluster
- Kustomize-based microservices deployment
- Secure cross-region connectivity using VPC peering
- Live health and sync status monitoring via ArgoCD UI

---

## How It Works

1. Both EKS clusters are registered in ArgoCD.
2. An ApplicationSet defines cluster targets and source configuration.
3. ArgoCD dynamically creates Applications for each cluster.
4. Sock Shop microservices are deployed using Kustomize.
5. Application health and sync status are continuously monitored.

---

## Tech Stack

- ArgoCD
- ApplicationSet Controller
- Amazon EKS
- Kubernetes
- Kustomize
- AWS VPC Peering
- GitOps
- Docker

---

## Key Benefits of ApplicationSet

- Simplifies multi-cluster GitOps
- Reduces manual configuration
- Enables scalable deployments
- Prevents configuration drift
- Ideal for multi-region Kubernetes platforms

---

## Future Enhancements

- Add environment-specific overlays
- Enable TLS with cert-manager
- Integrate Argo Rollouts for progressive delivery
- Extend to additional clusters and regions
