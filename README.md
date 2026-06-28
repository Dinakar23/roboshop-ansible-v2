# 🚀 Roboshop Microservices Deployment using Ansible on AWS

## 📌 Project Overview

This project demonstrates the complete automation of the **Roboshop Microservices Application** deployment on **AWS EC2** using **Ansible**.

The project follows Infrastructure as Code (IaC) principles by automating the installation, configuration, and deployment of multiple services using reusable **Ansible Roles**.

Sensitive credentials are secured using **Ansible Vault** and **AWS Secrets Manager**, making the deployment more secure and production-oriented.

---

# 🏗️ Architecture

The project deploys the following components:

* Frontend (Nginx)
* Catalogue Service
* User Service
* Cart Service
* Shipping Service
* Payment Service
* MongoDB
* MySQL
* Redis
* RabbitMQ

Each component is deployed on a dedicated AWS EC2 instance.

---

# ⚙️ Technologies Used

* AWS EC2
* AWS Route53
* AWS Secrets Manager
* Linux (RHEL 9)
* Ansible
* Ansible Roles
* Ansible Vault
* Dynamic Inventory
* Git & GitHub
* Nginx
* MongoDB
* MySQL
* Redis
* RabbitMQ
* NodeJS
* Java
* Python

---

# 📂 Project Structure

```
roboshop-ansible/
│
├── inventory/
├── group_vars/
├── roles/
│   ├── frontend/
│   ├── catalogue/
│   ├── user/
│   ├── cart/
│   ├── shipping/
│   ├── payment/
│   ├── mongodb/
│   ├── mysql/
│   ├── redis/
│   └── rabbitmq/
│
├── roboshop.yaml
├── ansible.cfg
└── README.md
```

---

# 🔐 Security Features

### ✅ Ansible Vault

Used to encrypt sensitive variables such as:

* Database Passwords
* Application Secrets
* Credentials

Example:

```
ansible-vault create vault.yaml
```

Run playbook:

```
ansible-playbook roboshop.yaml --ask-vault-pass
```

---

### ✅ AWS Secrets Manager

Database credentials are securely retrieved during deployment.

Example:

```
lookup('amazon.aws.aws_secret')
```

No passwords are stored directly inside playbooks.

---

# 📌 Key Features

* Automated deployment of Roboshop microservices
* Infrastructure as Code (IaC)
* Modular Ansible Roles
* Dynamic Inventory
* Route53 DNS automation
* Secure credential management using Ansible Vault
* AWS Secrets Manager integration
* Idempotent playbooks
* Automated service configuration
* Easy to maintain and reusable code

---

# 📌 Project Workflow

```
Developer
     │
     ▼
GitHub Repository
     │
     ▼
Ansible Control Node
     │
     ▼
Dynamic Inventory
     │
     ▼
AWS EC2 Instances
     │
     ▼
Configure Services
     │
     ▼
Deploy Roboshop Application
```

---

# 🚀 Deployment Steps

Clone Repository

```
git clone https://github.com/Dinakar23/roboshop-ansible.git
```

Move to project

```
cd roboshop-ansible
```

Install collections

```
ansible-galaxy collection install amazon.aws
```

Run playbook

```
ansible-playbook roboshop.yaml
```

Or deploy a single component

```
ansible-playbook roboshop.yaml -e "component=frontend"
```

---

# 🔄 Dynamic Inventory

The project supports Dynamic Inventory for AWS.

Benefits:

* Automatically discovers EC2 instances
* No need to manually update inventory
* Scalable deployment
* Supports cloud-native infrastructure

---

# 🔐 Secret Management

This project demonstrates two methods of managing secrets:

* Ansible Vault
* AWS Secrets Manager

This avoids storing passwords directly inside playbooks.

---

# 📈 Skills Demonstrated

* Linux Administration
* AWS Cloud
* Infrastructure as Code (IaC)
* Configuration Management
* Ansible Roles
* Dynamic Inventory
* Secret Management
* DNS Management
* Microservices Deployment
* Automation
* Troubleshooting
* Production-style Infrastructure

---

# 📚 What I Learned

During this project I gained practical experience in:

* Infrastructure Automation
* Configuration Management
* Linux Troubleshooting
* AWS Networking
* Route53 DNS Configuration
* Service Management
* Secure Secret Handling
* Reusable Ansible Roles
* Dynamic Inventory
* Cloud Deployment Best Practices

---

# 🎯 Future Improvements

* Dockerize each microservice
* Kubernetes Deployment
* Jenkins CI/CD Pipeline
* Terraform Infrastructure Provisioning
* Prometheus Monitoring
* Grafana Dashboard
* ELK Stack Logging
* AWS Load Balancer
* Auto Scaling Group

---

# 👨‍💻 Author

**Gaddam Dinakar**

Cloud | Linux | AWS | DevOps Engineer

📧 Email: [dinakargaddam23@gmail.com](mailto:dinakargaddam23@gmail.com)

🔗 LinkedIn: https://linkedin.com/in/g-dinakar-9a250b1a0

💻 GitHub: https://github.com/Dinakar23

---

## ⭐ If you found this project useful, don't forget to Star the repository!
