# Ericsson Cloud RAN Challenge
Kubernetes deployment of the hello-app application with Helm chart packaging.

## Prerequisites
- kubectl
- minikube
- Docker Engine
- Helm

## Repository Structure
```
├── hello-app.yaml      # Kubernetes manifest
└── hello-app/          # Helm chart directory
    ├── Chart.yaml
    ├── values.yaml
    └── templates/
        └── deployment.yaml
```

## Deployment

**Option 1: Kubernetes manifest**
```bash
kubectl apply -f hello-app.yaml
```

**Option 2: Helm chart**
```bash
helm install hello-app ./hello-app
```

## Test

Access the application:
```bash
curl http://<ip>:8080
```