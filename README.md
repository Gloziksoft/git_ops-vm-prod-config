# git_ops-vm-prod-config

## Purpose
This repository contains **production infrastructure configuration**
for a **VM-based environment**.

It reflects the **current production reality**:
- applications run on a single VM
- Docker Compose is used
- Kubernetes is NOT used in production

## Scope
This repository includes:
- infrastructure configuration
- ingress configuration
- VM-level and container-level monitoring
- production-related YAML and config files

## What this repository is NOT
- ❌ Kubernetes (k8s) production repository
- ❌ k3s configuration
- ❌ local / lab setup
- ❌ application source code

## Architecture overview
- Production runs on a VM
- Services are deployed using Docker Compose
- Monitoring (Prometheus / Grafana) runs on the same VM
- Persistent data is handled via Docker volumes

## History note
This repository was originally planned for Kubernetes,
but due to production constraints the final solution uses
Docker Compose on a VM.

The repository name reflects the **actual production setup**.

## Related repositories
- `git_ops-k3s-local-config` – local / lab Kubernetes (k3s)
- (future) `git_ops-k8s-prod-config` – Kubernetes production, if adopted

## Important rule
This repository should remain aligned with **production reality**.
Do not add Kubernetes manifests here unless production migrates to Kubernetes.
