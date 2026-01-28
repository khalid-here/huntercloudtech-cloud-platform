# HunterCloudTech — Cloud Engineering Project

Production-grade cloud infrastructure deployed on AWS using:

## Architecture
- VPC with Public & Private Subnets
- Application Load Balancer (ALB)
- Auto Scaling Group (ASG)
- CloudFront CDN
- AWS WAF
- Route 53 DNS
- ACM SSL
- CloudWatch Monitoring
- SNS Alerts

## Routing Strategy
- huntercloudtech.online → Main frontend
- app.huntercloudtech.online → Application UI
- api.huntercloudtech.online → API services
- huntercloudtech.online/admin → Admin Panel

## Security
- HTTPS via ACM
- AWS WAF with managed rule sets
- Private EC2 instances behind ALB
- IAM role-based access
- CloudWatch alarms

## Deployment
Hosted on Apache (Port 8080) behind ALB and CloudFront.

## Author
Mahaboob Basha  
Cloud Engineer | AWS | DevOps | Security

