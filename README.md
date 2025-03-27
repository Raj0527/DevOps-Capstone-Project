# DevOps-Capstone-Project

## **CI/CD Pipeline | Kubernetes | AWS | Terraform | Docker | Monitoring**  

### **Project Overview**  
This project demonstrates a **fully automated DevOps workflow** integrating:  
- **GitHub** – Version control & code repository  
- **Jenkins** – CI/CD automation for building, testing, and deployment  
- **Docker** – Containerization for backend & frontend  
- **Docker Hub** – Image repository  
- **Terraform** – Infrastructure as Code (IaC) to provision AWS resources  
- **Amazon EKS** – Kubernetes cluster for scalable deployments  
- **AWS CloudWatch** – Monitoring & alerting  

---

## **Project Workflow**  

### **1️⃣ Code Storage on GitHub**  
- The application source code is stored in **GitHub** for version control.  
- Jenkins is configured to pull the latest code from GitHub.  

### **2️⃣ Infrastructure Setup with Terraform**  
- Used **Terraform** to launch an **EC2 instance (Ubuntu)** for Jenkins.  
- Cloned the GitHub repository onto the EC2 instance.  
- Provisioned AWS resources:  
  - **VPC, subnets, security groups**  
  - **Amazon EKS Cluster** for deploying containers  

### **3️⃣ CI/CD Pipeline with Jenkins**  
- Created a **Jenkins pipeline** with the following stages:  
  - Clone the GitHub repository  
  - Build and test the application  
  - Create **Docker images** for backend and frontend  
  - Push images to **Docker Hub**  
  - Deploy containers on **Amazon EKS**  

### **4️⃣ Docker & Docker Hub**  
- Wrote **Dockerfiles** for both **backend and frontend**.  
- Built **Docker images** and pushed them to **Docker Hub** for easy deployment.  
- Created a **separate Jenkins pipeline** for:  
  - Backend Docker image build & push  
  - Frontend Docker image build & push  

### **5️⃣ Kubernetes Deployment with Amazon EKS**  
- Created an **Amazon EKS Cluster** using Terraform.  
- Deployed applications using **Kubernetes manifests**.  
- Exposed services for frontend and backend using **Kubernetes Services & Ingress**.  

### **6️⃣ Monitoring with AWS CloudWatch**  
- Configured **AWS CloudWatch** through Terraform to monitor:  
  - **EC2 instance performance** (CPU, memory usage)  
  - **EKS cluster health**  
  - **Application logs and alerts**  

---

