# Ericsson Cloud RAN Challenge
Kubernetes deployment of the hello-app application with Helm chart packaging.

## Prerequisites
- kubectl
- minikube
- Docker Engine
- Helm

## Repository Structure
```
.
├── hello-app.yaml      # Kubernetes manifest
└── hello-app/          # Helm chart directory
    ├── Chart.yaml
    ├── values.yaml
    └── templates/
        ├── deployment.yaml
        └── service.yaml
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

Note: You will need to set up a port forward for either option to make the app publicly accessible
```bash
kubectl port-forward service/hello-app 8080:8080 --address 0.0.0.0
```

## Test

Access the application:
```bash
curl http://<ip>:8080
```