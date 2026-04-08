# 🚀 TerraWeek Capstone Project – Multi-Environment Infrastructure with Terraform

## 📌 Project Overview

This project demonstrates how to build a **production-grade multi-environment infrastructure** using Terraform.

A single codebase is used to manage three environments:

* dev
* staging
* prod

Each environment is isolated and deployed using **Terraform Workspaces**.

---

## 🧱 Architecture

The infrastructure includes:

* VPC (Virtual Private Cloud)
* Public Subnet
* Internet Gateway
* Route Table
* Security Group
* EC2 Instance

Each environment has:

* Separate VPC (different CIDR)
* Separate EC2 instance (different instance types)
* Separate Terraform state

---

## 📁 Project Structure

```
terraweek-capstone/
│
├── main.tf
├── variables.tf
├── outputs.tf
├── providers.tf
├── locals.tf
│
├── dev.tfvars
├── staging.tfvars
├── prod.tfvars
│
├── modules/
│   ├── vpc/
│   ├── security-group/
│   └── ec2-instance/
│
└── .gitignore
```

---

## ⚙️ Key Features

✔ One codebase for multiple environments
✔ Terraform Workspaces for isolation
✔ Custom reusable modules
✔ Environment-specific configurations using tfvars
✔ Clean and scalable file structure
✔ Tagged resources (Project, Environment, ManagedBy)

---

## 🧠 Concepts Used

* Terraform Workspaces
* Modules (Custom Modules)
* Variables & tfvars
* Outputs
* Locals
* State Management
* AWS Infrastructure (VPC, EC2, Security Groups)

---

## 🚀 How to Run the Project

### 1. Initialize Terraform

```
terraform init
```

### 2. Create Workspaces

```
terraform workspace new dev
terraform workspace new staging
terraform workspace new prod
```

### 3. Deploy Environment

#### Dev

```
terraform workspace select dev
terraform apply -var-file="dev.tfvars"
```

#### Staging

```
terraform workspace select staging
terraform apply -var-file="staging.tfvars"
```

#### Prod

```
terraform workspace select prod
terraform apply -var-file="prod.tfvars"
```

---

## 🔍 Verification

* Each workspace creates separate infrastructure
* Different CIDR ranges for each VPC
* Different instance types per environment
* Resources visible in AWS Console

---

## 🧹 Cleanup

Destroy all environments:

```
terraform workspace select prod
terraform destroy -var-file="prod.tfvars"

terraform workspace select staging
terraform destroy -var-file="staging.tfvars"

terraform workspace select dev
terraform destroy -var-file="dev.tfvars"
```

---

## 📸 Screenshots

(Add your AWS Console and terraform output screenshots here)

---

## 📚 Learnings

* How to manage multiple environments using Terraform
* Importance of modular infrastructure
* Real-world project structure and best practices
* Infrastructure isolation using workspaces
* Clean and reusable Terraform code

---

## 🔗 GitHub Repository

https://github.com/Abhishek25singh25/Terraform-Capstone

---

## 🙌 Acknowledgement

This project is part of the **TerraWeek Challenge** under #90DaysOfDevOps

---

## 📢 Connect with Me

If you found this useful, feel free to connect and share feedback!

---

#️⃣ Tags
#Terraform #AWS #DevOps #InfrastructureAsCode #Cloud #90DaysOfDevOps
