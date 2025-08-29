
```markdown
# 🚀 ArgoCD Training with Nginx & Kubernetes

This repository contains **sample YAML manifests, Helm charts, and configurations** to practice **ArgoCD, Kubernetes, and Docker**.  
It is designed as a hands-on training repo for deploying and managing applications using GitOps principles.

---

## 📂 Repository Structure

```

argo-applications/       # Sample ArgoCD Application manifests
argocdappset/            # App-of-Apps / ApplicationSet examples
nginx/                   # Nginx deployment manifests
nginx-conf/              # Nginx custom configuration
nginx-helm/              # Nginx Helm chart example
nginx-pv/                # Persistent Volume examples
nginx-svc/               # Nginx Service (ClusterIP, NodePort, LoadBalancer)
nginx-sync/              # GitOps sync examples for Nginx

# Kubernetes learning resources

livenessprobe.yaml        # Example of liveness probe
resource-pod.yaml         # Resource limits/requests demo
antiaffinitypod.txt       # Pod anti-affinity example
Pod affinity.txt          # Pod affinity example
Preferred affinity.txt    # Preferred affinity rules
Tainttoleration.txt       # Taints & tolerations example
with-node-affinity.txt    # Node affinity rules
nodeselector.txt          # Node selector usage
startup probe.txt         # Startup probe config
Readinessprobes.txt       # Readiness probe config

# Docker learning materials

01-docker.ppt             # Intro to Docker
02-docker-basic-commands.doc
Docker Basics.pptx
Docker networking.pptx
Docker volumes.pptx
Docker compose.pptx
dockerfile-1.txt ... dockerfile-ml.txt
multistage.docx           # Multi-stage Docker builds
Dockermultiterapp.docx    # Multi-tier application with Docker
docker volume labs.txt    # Volume examples
docker netwokr lab 1/2    # Networking examples

# CI/CD & Jenkins

jenkinscript.txt
pipelinejob.xml
freestyleproj.xml
Jenkinsinstallation.docx

````

---

## 🛠️ Prerequisites

- [Docker](https://docs.docker.com/get-docker/)
- [Kubernetes](https://kubernetes.io/docs/setup/)
- [Kubectl](https://kubernetes.io/docs/tasks/tools/)
- [ArgoCD](https://argo-cd.readthedocs.io/en/stable/getting_started/)
- (Optional) [Helm](https://helm.sh/)

---

## 🚀 Getting Started

### Deploy ArgoCD (if not already installed)
```bash
kubectl create namespace argocd
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
````

### Access ArgoCD UI

```bash
kubectl port-forward svc/argocd-server -n argocd 8080:443
```

Open [https://localhost:8080](https://localhost:8080)

---

## ⚡ Example Workflows

### 1. Deploy Nginx with ArgoCD

```bash
kubectl apply -f argo-applications/nginx-app.yaml
```

### 2. Sync Application

ArgoCD will detect the app and deploy Nginx as defined in the manifests under `nginx/`.

### 3. Use Helm Chart

```bash
helm install my-nginx ./nginx-helm
```

---

## 📖 Training Content

This repo also contains **presentations, labs, and notes** covering:

* Docker basics, networking, and volumes
* Kubernetes pod scheduling, affinity/anti-affinity, probes
* ArgoCD ApplicationSet & GitOps workflows
* Jenkins pipelines for CI/CD

---

## 🔒 Notes

* This repository is intended for **training and practice**.
* Some files contain lab notes (`*.txt`, `*.docx`, `*.pptx`) rather than production-ready code.

---

## 🤝 Contributing

Feel free to fork, experiment, and submit pull requests if you’d like to enhance the training materials.

---

## 📜 License

This repository is for **educational purposes**. Use at your own risk.

```

