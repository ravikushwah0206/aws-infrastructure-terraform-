Secure AWS Multi-Tier Infrastructure & Landing Zone via Terraform

📌 Project Overview
This repository contains production-ready, declarative Infrastructure as Code (IaC) written in Terraform to provision a secure, highly available AWS Landing Zone. The architecture is engineered to act as a secure target environment for legacy-to-cloud and VMWare backup migrations, eliminating manual configuration drift and standard security gaps during deployment.


🛠️ Infrastructure Components Provisioned

- Networking: Custom VPC with isolated Public and Private Subnets across multiple Availability Zones to ensure high availability and application resilience.

- Compute & Orchestration: Amazon EKS (Elastic Kubernetes Service) cluster and worker nodes restricted entirely to private subnets to isolate workloads from the public internet.

- Security & Access Control:
  - Strict AWS IAM roles and policies enforcing the Principle of Least Privilege (PoLP).

  - Custom Security Groups acting as stateful firewalls, blocking all unauthorized inbound traffic.

- Data Protection Gateway: Configured target Amazon S3 storage buckets with server-side encryption enabled to securely accept enterprise backup snapshots (via Acronis/Symantec frameworks).

 🚀 Getting Started & Deployment

Prerequisites
- AWS CLI configured with appropriate IAM administrative permissions.
- Terraform CLI (v1.6+) installed locally.

Step-by-Step Execution
Initialize the working directory and download provider plugins:

terraform init

terraform plan

terraform apply -auto-approve
