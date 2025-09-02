# 🐳 Kubernetes Basic Web Setup

This project demonstrates how to deploy a simple static website using **Docker**, **Kubernetes**, and **Minikube**. It includes:

- A basic HTML website served via `nginx`
- Kubernetes Deployment and Service YAMLs
- Steps to build and expose the application on `localhost`

---

## 🛠️ Prerequisites

Make sure the following tools are installed and properly configured:

- [Docker Desktop](https://www.docker.com/products/docker-desktop)
- [Minikube](https://minikube.sigs.k8s.io/docs/)
- [kubectl](https://kubernetes.io/docs/tasks/tools/)

---

## 🚀 Getting Started

Follow these steps to run the project locally on Kubernetes via Minikube.

---

### 1. **Start Minikube**

```bash
minikube start
