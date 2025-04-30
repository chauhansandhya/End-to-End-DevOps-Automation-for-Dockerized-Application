# DevOps Lifecycle Automation for Monolithic Dockerized Application

This project implements a complete DevOps lifecycle to automate the deployment, scaling, and infrastructure provisioning of a monolithic web application using Jenkins, Docker, Kubernetes, and Terraform on AWS.

---

## 🧩 Project Overview

Analytics Pvt Ltd required a scalable and automated deployment solution for their Docker-based application hosted on GitHub. As the appointed DevOps Engineer, I was responsible for designing a CI/CD pipeline, provisioning infrastructure using Terraform, managing configurations, and deploying the application to a Kubernetes cluster on AWS — without modifying the existing Docker container used in testing.

---

## 🔧 Technologies Used

- **Source Control**: Git, GitHub
- **CI/CD**: Jenkins, AWS CodeBuild
- **Containerization**: Docker, Docker Hub
- **Orchestration**: Kubernetes (2 replicas, NodePort)
- **IaC**: Terraform (AWS)
- **Configuration Management**: Ansible (assumed)
- **Languages**: Shell scripting, YAML

---

## 🔁 DevOps Lifecycle Implemented

### ✅ Git Workflow
- Maintains version control of code in GitHub.
- Production releases scheduled for the **25th of every month**.
- Master branch is the release source.

### ⚙️ Continuous Integration (CI)
- CodeBuild and Jenkins pipelines trigger on push to `master`.
- Docker image is built automatically using the project’s `Dockerfile`.

### 📦 Containerization
- Docker images built and pushed to **Docker Hub** on each successful build.
- Custom Dockerfile ensures consistent container environments.

### 🚀 Continuous Deployment (CD)
- Deployed to **Kubernetes cluster** on AWS with:
  - 2 replicas
  - Exposed via **NodePort** on port `30008`

### ☁️ Infrastructure as Code (IaC)
- AWS infrastructure provisioned using **Terraform**:
  - EC2 instances, VPC, Security Groups
  - Jenkins host, K8s worker nodes

### ⚙️ Configuration Management
- Automated setup of tools on each worker node:
  - `Worker1`: Jenkins, Java
  - `Worker2`: Docker, Kubernetes
  - `Worker3`: Java, Docker, Kubernetes
  - `Worker4`: Docker, Kubernetes


## 📸 Architecture Diagram

> _Insert `architecture-diagram.png` here if available_  
> Shows Git ➝ Jenkins ➝ Docker ➝ Kubernetes ➝ AWS

## 📄 License

This project is part of a DevOps training and implementation case study by Sandhya Chauhan. All rights reserved.

