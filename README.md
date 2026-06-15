# AWS Web Application Deployment

## Objective
The objective of this task is to deploy a simple web application on an Amazon EC2 instance within a Virtual Private Cloud (VPC). The task demonstrates the integration of compute and networking services in AWS.

## Architecture
User → Internet → Security Group → EC2 Instance → Apache Web Server → Web Application

## AWS Services Used
- Amazon EC2
- Amazon VPC
- Security Groups
- Apache HTTP Server

## Deployment Steps

### Step 1: Create VPC
- Created a custom VPC.
- Configured public subnet.
- Attached Internet Gateway.

### Step 2: Configure Security Group
Added inbound rules:
- SSH (Port 22)
- HTTP (Port 80)

### Step 3: Launch EC2 Instance
- Selected Amazon Linux AMI.
- Chose t2.micro instance type.
- Attached the instance to the created VPC.

### Step 4: Install Web Server
Commands used:

```bash
sudo yum update -y
sudo yum install httpd -y
sudo systemctl start httpd
sudo systemctl enable httpd
