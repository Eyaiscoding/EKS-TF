# ☁️ EKS-TF: Terraform Infrastructure for SynchNotes

This repository contains the complete Infrastructure as Code (IaC) setup used to provision the AWS environment for the [SynchNotes](https://github.com/eyaiscoding/synchnotes) application — a secure, cloud-native collaboration tool built using DevSecOps and GitOps principles.

## ✅ Overview

The infrastructure is deployed using **Terraform** and includes:

- A fully managed **Amazon EKS cluster**
- Custom **VPC**, subnets, internet/NAT gateways, and routing
- **IAM roles and policies** for secure access control
- **EC2 instances** for Jenkins and SonarQube CI setup
- **Monitoring stack** with Prometheus, Grafana, and Datadog
- GitOps-ready integration with **ArgoCD**
- Best practices for security, observability, and scalability

---

## ⚙️ Prerequisites

- Terraform >= 1.3
- AWS CLI configured (`aws configure`)
- An active AWS account
- SSH key pair (for EC2 access, optional)

---

### 🚀 Deployment Steps

```bash
# 1. Clone the repo
git clone https://github.com/eyaiscoding/EKS-TF.git
cd EKS-TF

# 2. Initialize Terraform
terraform init

# 3. Check the execution plan
terraform plan

# 4. Apply infrastructure changes
terraform apply
