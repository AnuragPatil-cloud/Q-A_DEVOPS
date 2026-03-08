# ☁ AWS EC2 Interview Questions & Answers (DevOps)

This section contains commonly asked **Amazon EC2 interview questions for DevOps Engineers (Fresher – 2+ Years Experience).**

---

# 1. What is Amazon EC2?

Amazon EC2 (Elastic Compute Cloud) is a **virtual server service in AWS that allows users to run applications in the cloud**.

It provides **scalable computing capacity** without managing physical hardware.

---

# 2. What are the benefits of EC2?

Benefits include:

- Scalable infrastructure
- Pay-as-you-go pricing
- Full control over operating system
- Easy integration with AWS services
- High availability

---

# 3. What is an EC2 Instance?

An EC2 instance is a **virtual machine running in AWS cloud**.

It can run applications, web servers, databases, or any software.

Example uses:

- Web hosting
- Application servers
- CI/CD servers
- Microservices

---

# 4. What are EC2 Instance Types?

Instance types define **CPU, memory, storage, and networking capacity**.

Examples:

| Instance Type | Use Case |
|---------------|----------|
t2 / t3 | General purpose |
m5 | Balanced workloads |
c5 | Compute optimized |
r5 | Memory optimized |

---

# 5. What is an AMI?

AMI (Amazon Machine Image) is a **template used to create EC2 instances**.

It contains:

- Operating system
- Application software
- Configuration settings

Example:

```
Amazon Linux AMI
Ubuntu AMI
```

---

# 6. What is a Security Group?

A security group acts as a **virtual firewall for EC2 instances**.

It controls:

- Inbound traffic
- Outbound traffic

Example rules:

```
Allow SSH (22)
Allow HTTP (80)
Allow HTTPS (443)
```

---

# 7. What is a Key Pair?

A key pair is used to **securely connect to EC2 instances using SSH**.

Components:

- Public key → stored in AWS
- Private key → stored with user

Example connection:

```
ssh -i key.pem ubuntu@public-ip
```

---

# 8. What is Elastic IP?

Elastic IP is a **static public IP address used for EC2 instances**.

Benefits:

- Fixed public IP
- Can be reassigned to another instance

---

# 9. What is EBS?

EBS (Elastic Block Store) provides **persistent block storage for EC2 instances**.

Features:

- High performance
- Snapshot backups
- Persistent storage

---

# 10. What happens when an EC2 instance stops?

When an instance stops:

- Instance remains available
- Data on EBS remains
- Instance is not billed for compute

However:

- Public IP may change

---

# 11. What is EC2 Auto Scaling?

Auto Scaling automatically **increases or decreases the number of EC2 instances based on demand**.

Benefits:

- High availability
- Cost optimization

---

# 12. What is an Elastic Load Balancer?

ELB distributes incoming traffic across multiple EC2 instances.

Types:

- Application Load Balancer (ALB)
- Network Load Balancer (NLB)
- Classic Load Balancer

---

# 13. What is EC2 User Data?

User Data is a **script that runs automatically when an EC2 instance starts**.

Example:

```bash
#!/bin/bash
apt update -y
apt install nginx -y
systemctl start nginx
```

---

# 14. How do you connect to an EC2 instance?

Example:

```
ssh -i mykey.pem ubuntu@ec2-public-ip
```

---

# 15. What is EC2 Instance State?

EC2 instances have different states:

```
Pending
Running
Stopping
Stopped
Terminated
```

---

# 16. Real DevOps Scenario

### Problem

Application server running on EC2 is not accessible.

### Solution

Check:

1. Security group rules  
2. Instance status  
3. Application service running  
4. Network configuration

---

# 🚀 Why EC2 is Important for DevOps

DevOps engineers use EC2 for:

- Hosting applications
- Running CI/CD servers
- Running Kubernetes nodes
- Infrastructure automation

EC2 integrates with:

- AWS S3
- Load Balancers
- Auto Scaling
- Terraform
- Kubernetes
