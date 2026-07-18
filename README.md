# 🚀 End-to-End DevOps Project (Azure + AKS + Istio)

## 📖 About This Repository

This repository contains a **sample end-to-end DevOps application** created to help understand how different DevOps components work together.

The project demonstrates:

- Python Flask Application
- Docker Containerization
- GitHub Actions CI/CD
- Azure Container Registry (ACR)
- Azure Kubernetes Service (AKS)
- Kubernetes Manifests
- Istio Gateway & VirtualService

The code in this repository was built incrementally while explaining each component step by step. The primary goal is to **learn the complete deployment workflow**, not to provide a production-ready application.

---

## ⚠️ Important Note

This repository should be considered a **reference/demo project**.

The application and deployment files are intentionally simplified so that beginners can understand:

- How a Dockerfile is written
- How GitHub Actions CI/CD workflows are structured
- How Docker images are built and pushed
- How an application is deployed to AKS
- How Kubernetes manifests are organized
- How Istio Gateway and VirtualService expose applications

Before using this project in any real environment, additional changes, testing, security hardening, and infrastructure configuration will be required.

---

# 📁 Project Structure

```
azure-devops-aks-project
│
├── app/
│   ├── app.py
│   ├── templates/
│   ├── static/
│   └── requirements.txt
│
├── .github/
│   └── workflows/
│       └── deploy.yml
│
├── k8s/
│   ├── deployment.yaml
│   ├── service.yaml
│   ├── gateway.yaml
│   ├── virtualservice.yaml
│   ├── configmap.yaml
├── Dockerfile
├── .dockerignore
├── .gitignore
└── README.md
```

---

# 📂 Folder Description

## 📁 app/

Contains the sample Python Flask application.

**Purpose**

- Application source code
- HTML templates
- Static files
- Python dependencies

---

## 📁 .github/workflows/

Contains the GitHub Actions workflow.

**Purpose**

- Build Docker image
- Push image to Azure Container Registry
- Deploy application to AKS
- Verify deployment

---

## 📁 k8s/

Contains Kubernetes manifests.

**Purpose**

- Namespace
- ConfigMap
- Secret
- Deployment
- Service
- Istio Gateway
- VirtualService
- DestinationRule

---

## 📄 Dockerfile

Contains the instructions to build the application's Docker image.

This file demonstrates:

- Selecting a base image
- Installing dependencies
- Copying application files
- Exposing the application port
- Starting the application

---

# ⚠️ What This Repository Does NOT Include

This repository intentionally omits several production features, including:

- Terraform provisioning
- Helm charts
- GitOps (Argo CD / Flux CD)
- Azure Key Vault integration
- cert-manager
- Monitoring & Logging
- Multi-environment deployments
- Blue-Green or Canary deployments
- OIDC authentication
- Image signing
- Automated rollback
- Production-grade security hardening

These can be added as future enhancements depending on your requirements.

---

# 🎯 Purpose

The purpose of this repository is to help understand the complete DevOps workflow:

Application Code
→ Docker
→ GitHub Actions
→ Azure Container Registry
→ Azure Kubernetes Service
→ Kubernetes
→ Istio

Once you're comfortable with these concepts, you can extend this project by adding production-ready practices.