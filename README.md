# 🚀 Kubernetes Node.js Application (t3.small Optimized)

## 📌 Overview

This project demonstrates how to **build, containerize, and deploy a Node.js application on Kubernetes** using Minikube.
It is specifically optimized for **low-resource environments (AWS EC2 t3.small)**.

---

## 🧱 Architecture

```
User → NodePort (30007) → Service → Pod → Node.js App
```

---

## ⚙️ Tech Stack

* **Backend:** Node.js (Express)
* **Frontend:** HTML, CSS
* **Containerization:** Docker
* **Orchestration:** Kubernetes (Minikube)
* **CLI Tools:** kubectl

---

## 📁 Project Structure

```
k8s-node-app/
│
├── app.js
├── package.json
├── Dockerfile
├── index.html
├── style.css
│
├── k8s/
│   ├── deployment.yaml
│   └── service.yaml
│
└── README.md
```

---

## 🚀 Features

* ✅ Dockerized Node.js application
* ✅ Kubernetes Deployment with resource limits
* ✅ NodePort Service for external access
* ✅ Lightweight & optimized for 2GB RAM
* ✅ Frontend + Backend integration

---

## ⚙️ Prerequisites

Make sure you have installed:

* Docker
* Minikube
* kubectl
* Git

---
### 1️⃣ Install and configured all required files
k8s-node-app/
│
├── app.js
├── package.json
├── Dockerfile
├── index.html
├── style.css
│
├── k8s/
│   ├── deployment.yaml
│   └── service.yaml

### 2️⃣ Start Minikube (Optimized)

```
minikube start --driver=docker --memory=1400 --cpus=1
```

---

### 3️⃣ Use Minikube Docker

```
eval $(minikube docker-env)
```

---

### 4️⃣ Build Docker Image

```
docker build -t k8s-node-app .
```

---

### 5️⃣ Deploy to Kubernetes

```
kubectl apply -f k8s/deployment.yaml
kubectl apply -f k8s/service.yaml
```

---

### 6️⃣ Verify Deployment

```
kubectl get pods
kubectl get svc
```

---

## 🌐 Access Application

### 🔹 Option 1 (Recommended)

```
minikube service node-service
```

---

### 🔹 Option 2 (Manual Access)

Get IP:

```
minikube ip
```

Get port:

```
kubectl get svc
```

Open:

```
http://<minikube-ip>:30007
```

👉 Example:

```
http://192.168.49.2:30007
```

---

### 🔹 API Endpoint

```
http://<minikube-ip>:30007/api
```

👉 Output:

```
Backend is working perfectly 🚀
```

---

## 📊 Useful Kubernetes Commands

```
kubectl get pods
kubectl get svc
kubectl get deployments
kubectl describe pod <pod-name>
```

---

## ⚡ Optimization for t3.small

* Single replica deployment
* Resource limits (CPU & Memory)
* Alpine-based lightweight Docker image
* No heavy components (Ingress, Monitoring)

---





---
