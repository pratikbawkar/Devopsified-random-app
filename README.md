
# DevOpsifying a Python Flask Application — End-to-End CI/CD & GitOps on AWS EKS
This project demonstrates how a simple Python Flask application can be transformed into a complete DevOps workflow using Docker, Kubernetes, AWS EKS, Helm, GitHub Actions, Docker Hub, NGINX Ingress, and Argo CD.

## The project started as a basic calculator application with no containerization, CI/CD, or Kubernetes deployment practices.

## The final implementation provides:

- Docker containerization
- Multi-stage Docker build
- Kubernetes Deployment and Service
- AWS EKS deployment
- NGINX Ingress
- AWS Load Balancer
- Helm-based Kubernetes packaging
- GitHub Actions CI pipeline
- Flake8 code-quality checks
- Docker Hub image publishing
- Automatic image tagging
- Automatic Helm image-tag updates
- Argo CD GitOps-based deployment 

## Application

The application is a Python Flask calculator supporting:

- **Addition**
- **Subtraction**
- **Multiplication**
- **Division**
- **Division-by-zero handling**

Application port: 5000

The Flask application listens on:

**app.run(host="0.0.0.0", port=5000, debug=True)**

