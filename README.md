# Nginx Kubernetes Deployment

This project demonstrates a basic **Kubernetes Nginx setup** using core Kubernetes resources.
It is suitable for learning, practice.

---

## ⚙️ Components Overview

### Namespace
- Isolates all Nginx resources
- Name: `nginx`

### Deployment
- Runs **2 replicas** of Nginx
- Self-healing and scalable

### Service
- Type: `ClusterIP`
- Exposes Nginx internally on port `80`

### Pod (Optional)
- Standalone Pod
- Used only for understanding Pod behavior
- Not recommended for production

---

## 📌 Prerequisites

- Docker
- Kubernetes cluster (Kind / Minikube / Cloud)
- `kubectl` configured

---
## Step 1: Check the Service Name
kubectl get svc -n nginx

## Step 2: Forward Port
kubectl port-forward svc/nginx-service 8080:80 -n nginx

##Step 3: Access in Browser
http://localhost:8080

## 🚀 How to Run

```bash
kubectl apply -f namespace.yml
kubectl apply -f deployment.yml
kubectl apply -f service.yml

