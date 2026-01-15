# Nginx Kubernetes Deployment

This project demonstrates a basic **Kubernetes Nginx setup** using core Kubernetes resources.
It is suitable for learning, practice, and GitHub portfolio showcase.

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

## 🚀 How to Run

```bash
kubectl apply -f namespace.yml
kubectl apply -f deployment.yml
kubectl apply -f service.yml

