# 3_Tier_App_Terraform

Creating Terraform template to provision:

1. VPC Setup
    a. VPC with public and private subnets across 2 AZs
    b. Internet Gateway and NAT Gateway
    c. Route tables with appropriate routing
2. Application Infrastructure
    a. Application Load Balancer in public subnets
    b. Auto Scaling Group with EC2 instances in private subnets
    c. RDS Pssql instance in private subnets
3. Security Groups
    a. ALB: Allow HTTP/HTTPS from internet
    b. EC2: Allow traffic only from ALB and SSH from bastion
    c. RDS: Allow access only from EC2 instances
    d. Bastion host in public subnet for SSH access
