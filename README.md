# Cloud-Native Food Delivery Platform
## DevOps Implementation using AWS, Docker, Kubernetes & CI/CD

---

## 📌 Project Overview

This project demonstrates a **complete DevOps implementation** for an online food
ordering and delivery platform inspired by real-world systems such as **Zomato**.

The **application source code** was referenced from an open-source project for learning purposes.  
The **entire DevOps lifecycle** — including CI/CD automation, containerization,
cloud infrastructure, Kubernetes orchestration, and monitoring — was **designed,
implemented, and executed independently by me**.

The goal of this project is to showcase **DevOps practices close to real production setups**, 
with a **scalable, automated, and highly available cloud-native system**.

---

## 💡 Why I Built This Project

I built this project to gain **hands-on experience with real-world DevOps workflows**, 
understand CI/CD pipelines, Kubernetes deployments, cloud infrastructure provisioning, 
and monitoring practices, while creating a project I could reliably deploy end-to-end.

---

## 🎯 Business Objectives

- Enable fast and reliable deployments to production
- Eliminate manual infrastructure and deployment steps
- Support horizontal scalability during peak traffic
- Provide real-time monitoring and observability
- Ensure system stability with rollback capabilities

---

## ⚠ Challenges Faced

- Encountered IAM permission issues while connecting Jenkins with EKS
- Debugged Docker image pull errors from ECR due to incorrect IAM role mapping
- Resolved Kubernetes pod crash loops caused by incorrect environment variables

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

**Architecture Diagram:**

![Architecture Diagram](diagrams/architecture.png)

> Suggested diagram: Show Jenkins → Docker → EKS → Users + Prometheus/Grafana + Terraform infrastructure. Tools like Draw.io, Lucidchart, or Figma can be used.

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

## 📸 CI/CD Pipeline & Monitoring

### Jenkins Pipeline
![Jenkins Pipeline](screenshots/jenkins-pipeline.png)

### Kubernetes Deployment
![EKS Pods](screenshots/eks-pods.png)

### Grafana Monitoring Dashboard
![Grafana Dashboard](screenshots/grafana-dashboard.png)

> Replace these placeholders with actual screenshots from your setup.

---

## 🛠 How to Run This Project

1. **Clone the repository**
```bash
git clone https://github.com/AkashPedraj/FoodAppZomato-DevOps.git
cd FoodAppZomato-DevOps
Provision infrastructure using Terraform

bash
Copy code
cd terraform
terraform init
terraform apply
This will create VPC, subnets, security groups, and the EKS cluster.

Configure AWS CLI

bash
Copy code
aws configure
Enter your AWS Access Key, Secret Key, region, and output format.

Build and push Docker images

bash
Copy code
cd ../docker
docker build -t foodapp-frontend .
docker tag foodapp-frontend:latest <AWS_ECR_URI>/foodapp-frontend:latest
docker push <AWS_ECR_URI>/foodapp-frontend:latest
Deploy application on Kubernetes

bash
Copy code
cd ../k8s
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
kubectl apply -f ingress.yaml
Verify deployments

bash
Copy code
kubectl get pods -n <namespace>
kubectl get services -n <namespace>
kubectl get ingress -n <namespace>
Access the application
Use the ingress DNS name to access the deployed app.

Monitor the system
Open Grafana and Prometheus dashboards to view metrics and alerts.

📂 Repository Structure
text
Copy code
FoodAppZomato-DevOps/
├── Jenkinsfile
├── docker/
│   └── Dockerfile
├── k8s/
│   ├── deployment.yaml
│   ├── service.yaml
│   └── ingress.yaml
├── terraform/
│   ├── main.tf
│   ├── vpc.tf
│   └── eks.tf
├── monitoring/
│   ├── prometheus.yaml
│   └── grafana-dashboard.json
├── diagrams/
│   └── architecture.png
├── screenshots/
│   ├── jenkins-pipeline.png
│   ├── eks-pods.png
│   └── grafana-dashboard.png
└── README.md
📜 Credits & Disclaimer
Application code was forked from an open-source project for learning purposes.

All DevOps implementation, CI/CD pipelines, Docker, Kubernetes, Terraform infrastructure, and monitoring setups were developed and executed independently by me.
