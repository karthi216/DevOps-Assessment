# 🚀 DevOps Next.js App

A production-ready Next.js application containerized with Docker, deployed via Kubernetes, and published to GitHub Container Registry (GHCR). Built for DevOps assessments and scalable cloud-native workflows.

---

## 🛠️ Tech Stack

- ⚛️ Next.js
- 🐳 Docker
- ☸️ Kubernetes
- 📦 GitHub Container Registry (GHCR)
- 🧪 Minikube (local cluster)

  ## 🛠️ Local Setup

### Prerequisites
- Docker
- Minikube
- kubectl
- GitHub account with GHCR access

### Steps
1. Clone the repo  
   `git clone https://github.com/karthi216/devops-nextjs-app.git`

2. Start Minikube  
   `minikube start`

3. Create namespace  
   `kubectl create namespace assessments-dev`

4. Apply manifests  
   `kubectl apply -f k8s/ --namespace=assessments-dev`

5. Launch app  
   `minikube service nextjs-service --namespace=assessments-dev`

ghcr.io/karthi216/devops-nextjs-app:latest
🧠 Health Check (Optional)
Add a route like /healthz to verify container readiness.

## 🔄 CI/CD with GitHub Actions

Every push to `main` triggers:
- Docker build
- Image push to GHCR
- Kubernetes-ready deployment

Workflow file: `.github/workflows/deploy.yml`

|-----------------|----------------|-------------|------------------------|
🎉  Opening service assessments-dev/nextjs-service in default browser...
👉  http://127.0.0.1:36929
🎉 GHCR IMG URL
👉 image: ghcr.io/karthi216/devops-nextjs-app:latest

## 📜 License

MIT © Karthik Reddy

## 🙌 Credits

Built for DevOps mastery, container orchestration, and founder-grade polish.
