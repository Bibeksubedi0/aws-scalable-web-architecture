# Step-by-Step Implementation

## Step 1: VPC Setup
- Created a custom VPC
- Configured public subnets
- Attached Internet Gateway
- Configured route tables

## Step 2: S3 Static Website
- Created S3 bucket
- Enabled static website hosting
- Uploaded index.html and error.html
- Configured bucket policy for public access

## Step 3: EC2 Setup
- Launched Ubuntu EC2 instance
- Configured security group (HTTP + SSH)
- Installed Nginx
- Deployed website files

## Step 4: Target Group
- Created target group with HTTP protocol
- Registered EC2 instance
- Configured health checks

## Step 5: Application Load Balancer
- Created ALB with two public subnets
- Configured listener (HTTP)
- Attached target group

## Step 6: Auto Scaling
- Created launch template
- Configured Auto Scaling group
- Attached target group to ASG

