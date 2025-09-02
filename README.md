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
Initialize the Minikube Kubernetes cluster:

```bash
minikube start

### 2. **Build Docker Image**
Build an image from your Dockerfile:

```bash
docker image build -t simple-webpage .

### 3. **Deploy Application**
Apply the deployment configuration file:

```bash
kubectl apply -f ./nginx-deployment.yml

### 4. **Deploy Service**
Apply the service configuration file:

```bash
kubectl apply -f ./nginx-service.yml

### 5. ** Forward Local Port**
Expose the application on your localhost:

```bash
kubectl port-forward service/nginx-web-service 8080:80

Now, access your application at http://localhost:8080 in a web browser.


Verify deployment and service status with:
```bash
kubectl get pods
kubectl get services
