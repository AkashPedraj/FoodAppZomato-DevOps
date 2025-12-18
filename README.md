# Cloud-Native Food Delivery Platform  
## DevOps Implementation using AWS, Docker, Kubernetes & CI/CD

---

## 📌 Project Overview

This project demonstrates a **complete DevOps implementation** for an online food
ordering and delivery platform inspired by real-world systems such as **Zomato**.

The **application source code** was referenced from an open-source project for learning
purposes.  
The **entire DevOps lifecycle** — including CI/CD automation, containerization,
cloud infrastructure, Kubernetes orchestration, and monitoring — was **designed,
implemented, and executed independently by me**.

The goal of this project is to showcase **production-ready DevOps practices** for
building a **scalable, automated, and highly available cloud-native system**.

---

## 🎯 Business Objectives

- Enable fast and reliable deployments to production
- Eliminate manual infrastructure and deployment steps
- Support horizontal scalability during peak traffic
- Provide real-time monitoring and observability
- Ensure system stability with rollback capabilities

---

## 🧠 Scope of Work (My DevOps Responsibilities)

- Designed and implemented **end-to-end CI/CD pipelines** using Jenkins
- Integrated **GitHub Webhooks** for automated pipeline triggers
- Containerized application services using **Docker**
- Built and pushed Docker images to **AWS ECR**
- Provisioned cloud infrastructure using **Terraform**
- Deployed microservices to **AWS EKS** using Kubernetes
- Configured Kubernetes **auto-scaling and high availability**
- Implemented **monitoring and alerting** using Prometheus and Grafana
- Ensured environment separation for staging and production deployments

---

## 🏗 High-Level Architecture

**Cloud Provider:** AWS  

**Core Components:**
- EC2 (Jenkins & supporting services)
- EKS (Kubernetes cluster)
- ECR (Container registry)
- VPC, Subnets, Security Groups
- IAM Roles & Policies

**DevOps Stack:**
- Jenkins – CI/CD automation
- Docker – Containerization
- Kubernetes – Orchestration
- Terraform – Infrastructure as Code
- Prometheus – Metrics collection
- Grafana – Visualization & monitoring

📌 Refer to `diagrams/architecture.png` for the complete architecture diagram.

---

## 🚀 CI/CD Pipeline Workflow

1. Developer pushes code to GitHub repository
2. GitHub Webhook triggers Jenkins pipeline automatically
3. Jenkins pulls the latest code
4. Docker images are built for application services
5. Images are pushed to AWS ECR
6. Kubernetes manifests are applied to AWS EKS cluster
7. Application is deployed to staging environment
8. Prometheus collects application and system metrics
9. Grafana visualizes metrics via dashboards
10. Successful builds are promoted to production
11. Kubernetes auto-scaling ensures high availability

---

## 📂 Repository Structure

```text
FoodAppZomato-DevOps/
│
├── Jenkinsfile
├── docker/
│   └── Dockerfile
│
├── k8s/
│   ├── deployment.yaml
│   ├── service.yaml
│   └── ingress.yaml
│
├── terraform/
│   ├── main.tf
│   ├── vpc.tf
│   └── eks.tf
│
├── monitoring/
│   ├── prometheus.yaml
│   └── grafana-dashboard.json
│
├── diagrams/
│   └── architecture.png
│
└── README.md
