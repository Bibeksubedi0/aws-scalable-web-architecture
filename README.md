# AWS Scalable Web Architecture

## Project Overview
This project demonstrates a scalable and highly available web application architecture on AWS using core cloud services.

The architecture includes static website hosting using S3, compute using EC2, traffic distribution using Application Load Balancer, and automatic scaling using Auto Scaling Group.

## Services Used
- Amazon S3 (Static Website Hosting)
- Amazon EC2 (Ubuntu + Nginx)
- Application Load Balancer (ALB)
- Auto Scaling Group (ASG)
- VPC (Public Subnets, Route Tables, Internet Gateway)
- Security Groups

## Key Features
- High Availability using Multi-AZ deployment
- Load Balancing using ALB
- Auto Scaling for handling traffic spikes
- Static website hosting using S3
- Secure access using Security Groups

## Implementation Details
Detailed steps are documented in:
- docs/steps.md
- docs/commands.md
- docs/architecture.md

## Challenges Faced
- EC2 Connect failed due to incorrect SSH rules
- ALB required at least 2 public subnets
- S3 static website returned Access Denied errors
## Solutions
- Updated security groups to allow SSH properly
- Created second public subnet in a different Availability Zone
- Fixed S3 bucket policy and routing configuration

## Key Learnings
- Difference between public and private subnets
- How Load Balancer distributes traffic
- Importance of security groups
- How Auto Scaling works
- S3 static hosting behavior
