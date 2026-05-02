# AWS Multi-Tier DevOps Deployment with Load Balancer

## Project Overview
Built a production-style multi-tier cloud infrastructure on AWS from scratch.
The architecture includes a custom VPC with public and private subnets across
two Availability Zones, an Application Load Balancer routing traffic to
Docker-containerised EC2 instances, a Jenkins CI/CD pipeline automating
deployments, and CloudWatch monitoring — all secured with IAM roles and
Security Groups.

## Architecture
- VPC with public and private subnets across 2 Availability Zones
- Application Load Balancer (ALB) distributing traffic to private EC2 instances
- NAT Gateway for secure outbound internet access from private subnets
- Docker containerised Python Flask application deployed on EC2
- Jenkins Freestyle CI/CD pipeline automating build and deployment
- CloudWatch for infrastructure monitoring and alerting
- IAM roles and Security Groups enforcing least-privilege access

## Tech Stack
| Tool | Purpose |
|------|---------|
| AWS EC2 | Application servers in private subnets |
| AWS VPC | Network isolation and routing |
| AWS ALB | Load balancing and traffic distribution |
| AWS IAM | Access control and permissions |
| AWS CloudWatch | Monitoring and alerting |
| Docker | Application containerisation |
| Jenkins | CI/CD pipeline automation |
| Python Flask | Web application |
| Git | Version control |

## Project Steps

### Step 1 — VPC & Network Setup
- Created VPC with CIDR block
- Created public subnets (for ALB) and private subnets (for EC2) across 2 AZs
- Attached Internet Gateway to VPC
- Configured NAT Gateway in public subnet for private instance outbound access
- Set up route tables for public and private subnets

### Step 2 — EC2 & Security Groups
- Launched EC2 instances in private subnets
- Configured Security Groups: ALB allows port 80 from internet, EC2 allows port 80 only from ALB

### Step 3 — Application Load Balancer
- Created ALB in public subnets
- Created Target Group pointing to private EC2 instances
- Configured health checks and listener rules

### Step 4 — Docker & Application Deployment
- Built Docker image from Python Flask app using Dockerfile
- Ran container on EC2 instances mapping port 80

### Step 5 — Jenkins CI/CD Pipeline
- Installed Jenkins on EC2
- Created Freestyle job to pull code, build Docker image, and deploy container
- Verified successful build and deployment via Jenkins console output

### Step 6 — Monitoring
- Configured CloudWatch to monitor EC2 CPU, network, and status checks

## Screenshots

### VPC Architecture
![VPC](vpc-architecture.jpeg)

### Subnets
![Subnets](Subnets.jpeg)

### Application Load Balancer
![ALB](alb.jpeg)

### Target Group
![Target Group](Target-Group.jpeg)

### EC2 Instances
![EC2](EC2-Instances.jpeg)

### Jenkins CI/CD — Successful Build
![Jenkins](Jenkins-success.jpeg)

### Docker Container Running
![Docker](docker-running.jpeg)

### CloudWatch Monitoring
![CloudWatch](Cloud-Watch.jpeg)

### Final Output
![Output 1](Final-Output-1.jpeg)
![Output 2](Final-Output-2.jpeg)

## Key Learnings
- How public/private subnet architecture protects application servers
- How ALB health checks and target groups work in practice
- How Jenkins automates Docker build and deployment end-to-end
- How IAM roles replace hardcoded credentials for secure AWS access
- How NAT Gateway enables outbound access without exposing private instances

## Author
**Ashfaque Hurzuk**
Cloud & DevOps Engineer | Navi Mumbai
[LinkedIn](https://www.linkedin.com/in/ashfaque-hurzuk-a2b8a637a)
