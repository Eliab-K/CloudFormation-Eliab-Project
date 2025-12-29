# CloudFormation-Eliab-Project
Overview
CloudFormation-Eliab-Project demonstrates the deployment of a secure, scalable static website on AWS using Infrastructure as Code (IaC) principles. The project leverages AWS CloudFormation, Amazon S3, and Amazon CloudFront to deliver a globally distributed static website with improved performance, security, and reliability.
This repository serves as a practical example of how to provision cloud resources in a repeatable, automated, and production-aligned manner.
Architecture Summary
The solution provisions and integrates the following AWS services:
Amazon S3
Hosts static website content (HTML files)
Configured for static website hosting
Amazon CloudFront
Acts as a global Content Delivery Network (CDN)
Improves performance and reduces latency
Secures access to S3 content
AWS CloudFormation
Defines infrastructure using declarative templates
Enables repeatable and version-controlled deployments
GitHub Actions
Automates deployment workflows (CI/CD)
High-Level Architecture Diagram (Conceptual)
User Browser
     |
     v
CloudFront Distribution
     |
     v
S3 Static Website Bucket
Repository Structure
CloudFormation-Eliab-Project/
├── .github/workflows/        # GitHub Actions CI/CD workflows
├── CNAME                     # Custom domain configuration
├── Eliab.cfn.index.html      # CloudFormation-related HTML template
├── eliab.cf.s3.index.html    # S3 static website HTML content
├── README.md                 # Project documentation
Key Features
Infrastructure as Code using CloudFormation
Static website hosting on Amazon S3
Global content delivery via CloudFront
CI/CD automation using GitHub Actions
Custom domain support via CNAME
Cloud-ready and production-aligned design
Prerequisites
To deploy or modify this project, you should have:
An AWS account
AWS CLI configured (aws configure)
IAM permissions for:
CloudFormation
S3
CloudFront
Basic knowledge of AWS and HTML
GitHub account (for CI/CD workflows)
Deployment Workflow
1. Clone the Repository
git clone https://github.com/Eliab-K/CloudFormation-Eliab-Project.git
cd CloudFormation-Eliab-Project
2. Review Templates
Validate HTML files for static content
Review CloudFormation-related configuration logic
Confirm CloudFront and S3 configurations align with your region and needs
3. Deploy via CloudFormation
Deploy the stack using either:
AWS Management Console, or
AWS CLI
Example (CLI-based deployment):
aws cloudformation deploy \
  --template-file template.yaml \
  --stack-name eliab-static-site \
  --capabilities CAPABILITY_NAMED_IAM
(Adjust template names as applicable)
CI/CD Automation
The .github/workflows directory contains GitHub Actions workflows that enable:
Automated validation of changes
Continuous deployment of static content
Reduced manual deployment effort
Improved consistency across environments
Custom Domain Configuration
The CNAME file allows mapping a custom domain to the CloudFront distribution
DNS configuration must be completed at the domain registrar or Route 53
HTTPS can be enabled via AWS Certificate Manager (ACM)
Security Considerations
CloudFront restricts direct access to S3
Public access can be controlled at the bucket policy level
HTTPS support via CloudFront + ACM
Infrastructure changes are version-controlled
Use Cases
Personal or professional portfolio website
Static corporate or informational websites
CloudFormation learning reference
DevOps / Cloud Engineering demonstrations
Lightweight production static hosting
Author
Eliab K (Engineer Kisienya)
Infrastructure & Cloud Engineer
GitHub: https://github.com/Eliab-K
Focus Areas:
AWS & Cloud Architecture
Infrastructure as Code (IaC)
DevOps & CI/CD
Security & High Availability Systems
License
This project is open for learning and demonstration purposes.
You are free to fork and adapt it with proper attribution.
