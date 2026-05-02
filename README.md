# AWS Multi-Tier DevOps Deployment with Load Balancer

## Project Overview
What this project does in 3–4 sentences.

## Architecture
- VPC with public/private subnets across 2 AZs
- ALB routing traffic to EC2 instances in private subnets
- Docker containerised Flask app deployed on EC2
- Jenkins CI/CD pipeline automating build & deploy
- NAT Gateway for outbound access from private instances
- CloudWatch for monitoring, IAM + Security Groups for access control

## Tech Stack
AWS (EC2, VPC, ALB, IAM, NAT Gateway, CloudWatch) | Docker | Jenkins | Python Flask | Git

## Project Setup & Steps
Step 1: VPC and subnet creation
Step 2: EC2 launch in private subnets
Step 3: ALB configuration and target groups
Step 4: Docker image build and deployment
Step 5: Jenkins pipeline setup
Step 6: CloudWatch monitoring setup

## 📸 Project Screenshots

### 🧱 VPC Architecture
![VPC](./vpc-architecture.jpeg)

### 🌐 Subnets
![Subnets](./Subnets.jpeg)

### ⚖️ Application Load Balancer
![ALB](./alb.jpeg)

### 🎯 Target Group
![Target Group](./Target-Group.jpeg)

### 🖥️ EC2 Instances
![EC2 Instances](./EC2-Instances.jpeg)

### 🔁 Jenkins CI/CD Pipeline
![Jenkins](./Jenkins-success.jpeg)

### 🐳 Docker Container Running
![Docker](./docker-running.jpeg)

### 📊 CloudWatch Monitoring
![CloudWatch](./Cloud-Watch.jpeg)

### 🌍 Final Output

![Final Output 1](./Final-Output-1.jpeg)

![Final Output 2](./Final-Output-2.jpeg)
