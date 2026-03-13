# 🌐 AWS VPC Scenario-Based DevOps Interview Questions

This section contains **real-world AWS VPC troubleshooting scenarios** commonly faced by DevOps engineers.

---

# Scenario 1: EC2 Instance in Private Subnet Cannot Access Internet

### Problem
An EC2 instance in a private subnet cannot access the internet for updates.

### Possible Causes

- No NAT Gateway configured
- Incorrect route table
- Security group restrictions

### Solution

1. Create a NAT Gateway in a public subnet.
2. Update the private subnet route table:

```
0.0.0.0/0 → NAT Gateway
```

This allows private instances to access the internet without exposing them publicly.

---

# Scenario 2: Public EC2 Instance Not Accessible from Internet

### Problem
You cannot access a public EC2 instance using SSH or HTTP.

### Possible Causes

- Security group blocking traffic
- Internet Gateway not attached
- Route table misconfiguration

### Solution

Check:

Security group rules:

```
Allow SSH (22)
Allow HTTP (80)
```

Verify route table:

```
0.0.0.0/0 → Internet Gateway
```

Ensure the instance has a public IP.

---

# Scenario 3: Instances in Two Subnets Cannot Communicate

### Problem
Two EC2 instances in different subnets within the same VPC cannot communicate.

### Possible Causes

- Security group blocking traffic
- Network ACL restrictions
- Incorrect route table

### Solution

Check:

- Security group inbound rules
- Network ACL rules
- VPC routing configuration

Allow required ports between the instances.

---

# Scenario 4: NAT Gateway Not Working

### Problem
Private instances cannot access the internet even though NAT Gateway exists.

### Possible Causes

- NAT Gateway created in wrong subnet
- Incorrect route table configuration
- Security group restrictions

### Solution

Verify:

```
Private subnet route table → NAT Gateway
```

Ensure NAT Gateway is deployed in a **public subnet**.

---

# Scenario 5: Load Balancer Not Reachable

### Problem
Application Load Balancer is not accessible via DNS.

### Possible Causes

- Security group blocking traffic
- Incorrect subnet configuration
- Target instances unhealthy

### Solution

Check:

```
Target Group → Health Status
```

Ensure ALB is deployed in **public subnets** and security group allows traffic on port 80/443.

---

# Scenario 6: Cannot SSH into Private EC2 Instance

### Problem
You need to access an EC2 instance inside a private subnet.

### Solution

Use a **Bastion Host**.

Architecture:

```
Admin Laptop
      ↓
Bastion Host (Public Subnet)
      ↓
Private EC2 Instance
```

SSH example:

```
ssh -i key.pem ec2-user@bastion-ip
```

---

# Scenario 7: High Network Traffic in VPC

### Problem
Unexpected network traffic detected in VPC.

### Solution

Enable **VPC Flow Logs**.

Steps:

```
VPC → Flow Logs → Enable
```

Analyze logs using:

- CloudWatch
- S3
- Athena

---

# Scenario 8: Multiple VPCs Need to Communicate

### Problem
Two VPCs need to communicate securely.

### Solution

Use **VPC Peering**.

Steps:

1. Create VPC Peering connection.
2. Update route tables in both VPCs.

---

# Scenario 9: On-Premise Network Needs Access to AWS VPC

### Problem
Company data center must connect to AWS VPC.

### Solution

Use:

```
AWS Site-to-Site VPN
```

or

```
AWS Direct Connect
```

---

# Scenario 10: Private EC2 Needs to Access S3 Without Internet

### Problem
Private instances need to access S3 without using internet.

### Solution

Create **VPC Endpoint for S3**.

Benefits:

- private connectivity
- improved security
- no internet required

---

# 🎯 Why VPC Scenarios Are Important for DevOps

DevOps engineers working with AWS must troubleshoot:

- networking connectivity issues
- internet access problems
- load balancer routing
- subnet communication
- secure architecture design

Understanding VPC scenarios helps build **secure and scalable cloud infrastructure**.
