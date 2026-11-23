# AI DevOps Engineering – Environment Setup

## Project Overview

This project documents the installation, configuration, and verification of essential DevOps tools on an Ubuntu Linux environment.

The objective is to establish a functional development environment supporting version control, containerization, Kubernetes orchestration, Infrastructure as Code, configuration management, cloud administration, and application development.

## Operating Environment

- **Operating System:** Ubuntu Linux
- **Shell:** Bash
- **Package Managers:** APT, Snap (where applicable), and official vendor installation scripts
- **Containerization:** Docker and Docker Compose
- **Container Orchestration:** Kubernetes and Minikube
- **Cloud Platforms:** AWS and Microsoft Azure

## Tools Configured

| Tool | Purpose |
|---|---|
| Git | Source code version control |
| Visual Studio Code | Development environment |
| Docker | Containerization |
| Docker Compose | Multi-container application management |
| Kubernetes CLI (kubectl) | Kubernetes cluster administration |
| Minikube | Local Kubernetes environment |
| Terraform | Infrastructure as Code |
| Ansible | Configuration management and automation |
| AWS CLI | AWS cloud administration |
| Azure CLI | Microsoft Azure cloud administration |
| Node.js and npm | JavaScript runtime and package management |
| jq | JSON processing |

## Installation Methodology

The environment was prepared by updating Ubuntu packages and installing the required tools using APT, official software repositories, and vendor-provided installation methods.

Installation commands were executed in the terminal, followed by version checks to confirm successful installation.

## Troubleshooting

### Repository Configuration Errors

During installation, package repository errors were encountered for Docker and Kubernetes, including HTTP 404 errors.

Troubleshooting involved identifying invalid repository entries and reviewing the appropriate official package sources.

### AWS CLI Installation

An initial AWS CLI installation attempt failed because the installation script could not be found at the specified location.

The installation path and extracted package location were reviewed before retrying.

### Kubernetes Configuration

The local Kubernetes environment requires a functioning container runtime. Minikube was configured to use Docker as its driver, with cluster readiness checked using Kubernetes CLI commands.

## Verification

Tool installation was checked using version commands such as:

```bash
git --version
docker --version
docker compose version
kubectl version --client
minikube version
terraform --version
ansible --version
aws --version
az version
node --version
npm --version
jq --version
```

The results are recorded in `reports/tooling-verification.txt`.

Local Kubernetes functionality is verified using:

```bash
minikube status
kubectl get nodes -o wide
kubectl get pods -A
```

Screenshots are stored in the `screenshots/` directory.

## Deliverables

- [ ] Bash environment configuration file
- [ ] Tooling verification report
- [ ] Screenshot of installed tool versions
- [ ] Screenshot of running Minikube cluster
- [ ] Screenshot of Kubernetes node in Ready status
- [ ] Completed README documentation

## Learning Summary

This project provides practical experience in Linux administration, package management, DevOps tooling installation, troubleshooting, and environment verification.

It also establishes the foundational environment required for subsequent activities involving CI/CD pipelines, cloud infrastructure automation, container orchestration, and Infrastructure as Code.
