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

## 🗂 Project Structure

EKS-TF/
├── modules/                # Optional: reusable Terraform modules
├── jenkins.tf              # Jenkins and SonarQube EC2 provisioning
├── vpc.tf                  # VPC, subnets, route tables, gateways
├── eks.tf                  # EKS cluster, node groups, IAM roles
├── iam.tf                  # IAM roles and policies for services
├── monitoring.tf           # Prometheus, Grafana, Datadog setup
├── variables.tf            # Input variable declarations
├── outputs.tf              # Output values for use after deployment
├── providers.tf            # AWS provider setup
└── main.tf                 # Root module tying everything together


---

## ⚙️ Prerequisites

- Terraform >= 1.3
- AWS CLI configured (`aws configure`)
- An active AWS account
- SSH key pair (for EC2 access, optional)

---

## 🚀 Deployment Steps

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
