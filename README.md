# 📚 BookVerse — AWS 3-Tier Infrastructure with Terraform

### Infrastructure as Code | AWS | Terraform | DevOps

BookVerse is a cloud infrastructure project designed for a Book & Author Management application. The infrastructure is provisioned using Terraform and AWS, following a modular and multi-environment approach.

The project focuses on building reusable infrastructure components, simplifying deployment, and maintaining separate configurations for Development, Testing, and Production environments.

---

## 🎯 Project Objectives

- Provision AWS infrastructure using Terraform.
- Organize infrastructure into reusable Terraform modules.
- Maintain separate DEV, TEST, and PROD environments.
- Deploy frontend and backend compute infrastructure.
- Configure Auto Scaling Groups for application workloads.
- Automate infrastructure provisioning and management.
- Follow Infrastructure as Code best practices.

---

## 🛠️ Technology Stack

- **Cloud Platform:** Amazon Web Services (AWS)
- **Infrastructure as Code:** Terraform
- **Compute:** Amazon EC2
- **Scaling:** Auto Scaling Groups
- **Load Balancing:** Elastic Load Balancing
- **Networking:** Amazon VPC
- **Database:** Amazon RDS
- **Version Control:** Git and GitHub

---

## 🏗️ Infrastructure Implementation

### 1. Multi-Environment Configuration

The project is organized into three environments:

- **DEV:** For development and infrastructure experimentation.
- **TEST:** For testing and validating infrastructure changes.
- **PROD:** For production infrastructure.

Each environment has its own Terraform entry-point configuration.

### 2. Modular Terraform Architecture

The project uses a modular directory structure to organize infrastructure components.

Reusable modules help keep the configuration organized, maintainable, and easier to extend.

### 3. Frontend Infrastructure

The frontend infrastructure includes EC2-related configuration, launch templates, and Auto Scaling components.

These resources provide the foundation for hosting the BookVerse application frontend.

### 4. Backend Infrastructure

The backend infrastructure includes EC2 and Auto Scaling configurations for application workloads.

Separating frontend and backend resources allows each tier to be managed independently.

### 5. Networking and Security

The infrastructure configuration includes VPC-related components, subnets, and security groups.

These components establish network connectivity and control traffic between application resources.

### 6. Database Infrastructure

The project includes a dedicated database module for managing Amazon RDS resources.

The database configuration can be extended to support read replicas and other database requirements.

### 7. Infrastructure Automation

Terraform manages infrastructure through declarative configuration files.

The workflow includes initialization, validation, execution planning, and applying infrastructure changes.

### 8. Version Control

The project is maintained in Git and hosted on GitHub.

A `.gitignore` file helps exclude Terraform state files, local working directories, and sensitive configuration files from version control.

---

## 📂 Project Structure

```text
ROOT/
├── envs/
│   ├── dev/
│   │   └── main.tf
│   ├── test/
│   │   └── main.tf
│   └── prod/
│       └── main.tf
│
├── modules/
│   ├── backend/
│   │   ├── asg/
│   │   └── ec2/
│   ├── bastion/
│   ├── database/
│   └── frontend/
│       ├── asg/
│       ├── ec2/
│       └── launch-template/
│
└── .gitignore
