# DevOps EKS Project

## Application
React application deployed on AWS EKS using CI/CD pipeline.

**Repo:** https://github.com/Vennilavanguvi/Trend.git  
**Live URL:** http://a15ecdc0017e74e3893fd6977a834d97-1078967719.us-east-1.elb.amazonaws.com:3000

---

## Tech Stack
- Docker
- Terraform
- AWS EKS (Kubernetes)
- Jenkins
- GitHub
- Docker Hub
- Uptime Kuma (Monitoring)

---

## Pipeline Flow
Code Push → GitHub Webhook → Jenkins Trigger → Docker Build → DockerHub Push → kubectl apply → EKS Deploy → LoadBalancer → Users

---

## Setup Instructions

### 1. Clone Repository
git clone https://github.com/haritechhub/devops-eks.git
cd devops-eks

### 2. Terraform — Infrastructure Setup
cd terraform
terraform init
terraform plan
terraform apply

### 3. Configure kubectl
aws eks update-kubeconfig --name devops-eks-cluster --region us-east-1
kubectl get nodes

### 4. Jenkins Setup
- Install Jenkins on EC2
- Install Plugins: Docker Pipeline, GitHub Integration, AWS Credentials, Kubernetes CLI
- Add Credentials: DockerHub + AWS
- Create Pipeline: Point to GitHub repo
- Add GitHub Webhook

### 5. Deploy
git push origin dev
(Jenkins automatic trigger aagum!)

---

## Kubernetes
kubectl get pods
kubectl get services

---

## Monitoring
Uptime Kuma: http://JENKINS-EC2-IP:3001

---

## Screenshots
Screenshots folder la irukku!