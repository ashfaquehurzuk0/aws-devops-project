# AWS Multi-Tier DevOps Project (VPC + CI/CD + Docker + ALB)

## 🚀 Project Overview
This project demonstrates a real-world AWS cloud architecture using a multi-tier setup with secure networking, load balancing, containerized application deployment, and CI/CD automation using Jenkins.

---

## 🏗️ Architecture Summary

- Custom VPC with public and private subnets across multiple Availability Zones  
- Application Load Balancer (ALB) for traffic distribution  
- EC2 instances deployed in private subnets for application hosting  
- Jenkins server for CI/CD automation  
- Docker containerized application deployment  
- NAT Gateway for secure outbound internet access  
- CloudWatch for monitoring system performance  

---

## 📸 Project Screenshots

### 🧱 VPC Architecture
![VPC](./screenshots/vpc-architecture.jpeg)

### 🌐 Subnets
![Subnets](./screenshots/Subnets.jpeg)

### ⚖️ Application Load Balancer
![ALB](./screenshots/alb.jpeg)

### 🎯 Target Group
![Target Group](./screenshots/Target-Group.jpeg)

### 🖥️ EC2 Instances
![EC2 Instances](./screenshots/EC2-Instances.jpeg)

### 🔁 Jenkins CI/CD Pipeline
![Jenkins](./screenshots/Jenkins-success.jpeg)

### 🐳 Docker Container Running
![Docker](./screenshots/docker-running.jpeg)

### 📊 CloudWatch Monitoring
![CloudWatch](./screenshots/Cloud-Watch.jpeg)

### 🌍 Final Application Output

![Final Output 1](./screenshots/Final-Output-1.jpeg)

![Final Output 2](./screenshots/Final-Output-2.jpeg)

---

## 🔁 CI/CD Workflow

1. Code pushed to GitHub  
2. Jenkins pulls latest code  
3. Docker image is built  
4. Application deployed to EC2 instances  
5. ALB distributes traffic across healthy targets  

---

## 🔐 Security Implementation

- Private subnet architecture for application servers  
- Security Groups controlling inbound/outbound traffic  
- IAM roles for AWS access control  
- NAT Gateway for controlled internet access  

---

## 📊 Monitoring

- AWS CloudWatch for EC2 monitoring  
- CPU utilization tracking enabled  

---

## 🧠 Key Learnings

- Multi-tier AWS architecture design  
- Load balancing using ALB  
- CI/CD automation using Jenkins  
- Docker-based deployment  
- VPC networking (public/private subnets)  
- Cloud monitoring fundamentals  

---

## 📌 Tech Stack

- AWS (EC2, VPC, ALB, IAM, CloudWatch, NAT Gateway)  
- Jenkins  
- Docker  
- Linux  
- Git & GitHub  

---

## 👤 Author

Ashfaque  
Navi Mumbai, India
