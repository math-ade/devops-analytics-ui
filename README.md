# 🚀 Enterprise DevOps Platform Analytics & Cloud-Native Mesh

[![Kubernetes](https://shields.io)](https://kubernetes.io)
[![Ansible](https://shields.io)](https://ansible.com)
[![Docker](https://shields.io)](https://docker.com)
[![License](https://shields.io)](#)

An enterprise-grade, localized Platform Engineering lab showcasing end-to-end continuous deployment, infrastructure declarative configuration, visual cluster orchestration, and high-availability self-healing microservice topologies. 

This project demonstrates a resilient operational transition from classic monolithic container controls to a native, air-gapped **Linux CLI-Driven GitOps Cluster architecture**.

---

## 🏗️ Architectural Topology Overview

The cluster fabric decouples static server footprints from runtime application layers, establishing an isolated GitOps control loop:

1. **Source Code Plane (GitHub):** Version-controlled code definitions (`index.html`), pipeline scripts (`Jenkinsfile`), and server playbooks (`site.yml`).
2. **Configuration Orchestrator (Ansible Semaphore):** Decoupled web management engine running automated telemetry audits over static host inventories.
3. **Application Control Plane (Kubernetes/Minikube):** Microservice pod runtime executing declarative infrastructure blueprints natively over the Linux kernel.

---

## ☸️ Declarative Cluster Ingress Specifications

The application workspace uses native Kubernetes primitives to guarantee high availability and instant portability:

* **Deployment Replicas:** Spawns a high-availability pool of **5 load-balanced container nodes** running an optimized `nginx:alpine` engine.
* **Volume Configuration (ConfigMaps):** Immutably injects our dynamic DevOps Telemetry UI code right into the web container root (`/usr/share/nginx/html`) at runtime, preventing image bloat.
* **Service Networking (NodePort):** Securely opens a dedicated hardware ingress gateway on port `30080` to handle external traffic shifting safely.

---

## ⚡ Quick Deployment & Execution

To ingest this exact multi-resource blueprint directly into your active cluster control plane, execute the deployment manifest using your command-line interface:

```bash
# Ingest the unified manifest architecture
kubectl apply -f dashboard.yaml

# Verify the live state metrics inside the namespace
kubectl get deployments,services,pods -o wide
```

## 🛠️ Resiliency & Incident Remediation Log
During initial environment provisioning, the platform encountered an HTTP/2 protocol stream error (`PROTOCOL_ERROR`) from remote registries, which cached corrupted binary data fragments locally. 

**Remediation Action:** Bypassed traditional graphical hypervisor layers entirely, entered the native Linux subsystem kernel perimeter, purged the state cache directories using a full `minikube delete --all --purge` loop, and forced a fresh binary verification pass—achieving a pristine status line with **0 restarts** across active production runtimes.
