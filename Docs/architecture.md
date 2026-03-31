# Architecture Explanation

## Flow of Traffic

1. User sends request from browser
2. Request goes to Application Load Balancer
3. ALB distributes traffic to EC2 instances
4. EC2 instances serve the website using Nginx
5. Static content can also be served via S3

## Components

### S3
Used for static website hosting and storing assets.

### EC2
Hosts the web server and serves application content.

### ALB
Distributes incoming traffic across multiple EC2 instances.

### Auto Scaling
Automatically increases or decreases instances based on demand.

## High Availability
- Multiple subnets across different Availability Zones
- Load balancing ensures uptime