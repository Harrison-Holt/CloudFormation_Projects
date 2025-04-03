# ☁️ CloudFormation Projects

A collection of AWS CloudFormation templates I’ve written from scratch to provision secure, scalable infrastructure. These templates reflect real-world deployment needs and were built as part of my DevOps learning journey.

---

## 📌 Project Purpose

This repository showcases my ability to:

- Use Infrastructure as Code (IaC) to provision AWS resources
- Apply best practices in security, scalability, and automation
- Build reusable, production-grade templates
- Troubleshoot deployment failures and debug with AWS tools

---

## 🔥 Featured Template: Static Website with CloudFront & S3

This CloudFormation template provisions:

- A **private S3 bucket** for static website files  
- A **CloudFront distribution** using Origin Access Identity (OAI)  
- A **secure bucket policy** that only allows CloudFront to access S3  
- A globally distributed, HTTPS-accessible static website

### 🔗 Live Demo

🌐 [View Deployed Site](https://d1n6bcb0b174if.cloudfront.net)

### 📂 GitHub Repo

📁 [Static Site Template](https://github.com/Harrison-Holt/cloudformation-templates/blob/main/static-site-template.yaml)

---

## 🧩 Key AWS Services Used

- **Amazon S3** – For private file storage and static hosting
- **AWS CloudFront** – CDN for global distribution and HTTPS support
- **Origin Access Identity (OAI)** – Ensures secure access between CloudFront and S3
- **IAM** – Permissions and resource-based bucket policy
- **CloudFormation Stack Events** – For monitoring deployment status

---

## 🧠 Common Challenges Solved

- ✅ Used `DependsOn` to avoid race conditions between S3 and its BucketPolicy
- ✅ Corrected bucket `Resource` ARN to include `/*` for object-level access
- ✅ Validated stack success via CloudFormation Events tab and output URLs

---

## 🛣️ Template Roadmap (Coming Soon)

- [ ] VPC with public/private subnets and NAT Gateway  
- [ ] EC2-based web server with Auto Scaling  
- [ ] Lambda + S3 + SNS event-driven architecture  
- [ ] CI/CD pipeline using CodePipeline and CodeBuild 
