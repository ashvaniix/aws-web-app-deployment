# AWS EC2 Web Application Deployment

## Objective
Deploy a simple web application on an Amazon EC2 instance within a VPC and configure Security Groups for web access.

## Services Used
- Amazon VPC
- Amazon EC2
- Security Groups
- Apache Web Server

## Step 1: Create VPC
- Created a custom VPC.
- Configured a public subnet.
- Attached an Internet Gateway.
- Updated route tables.

## Step 2: Configure Security Group
- Allowed SSH access on Port 22.
- Allowed HTTP access on Port 80.

## Step 3: Launch EC2 Instance
- Selected Amazon Linux AMI.
- Chose t2.micro instance type.
- Attached Security Group.

## Step 4: Install Apache Web Server

```bash
sudo yum update -y
sudo yum install httpd -y
sudo systemctl start httpd
sudo systemctl enable httpd
```

## Step 5: Deploy Web Application

```html
<!DOCTYPE html>
<html>
<head>
<title>AWS Web App</title>
</head>
<body>
<h1>Hello from AWS EC2</h1>
<p>Web application deployed successfully.</p>
</body>
</html>
```

## Security Group Rules

| Type | Port |
|--------|--------|
| SSH | 22 |
| HTTP | 80 |

## Deliverables
- Running Web Application
- Deployment Documentation
- Security Group Configuration

## Challenges Faced
- Understanding VPC networking
- Configuring Security Groups
- Managing Apache Web Server
- Testing application connectivity

## Conclusion
Successfully deployed a web application on an EC2 instance inside a VPC and configured Security Groups for secure access.
