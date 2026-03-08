# 🚀 AWS EC2 Real DevOps Scenario-Based Interview Questions

This section contains **real-world DevOps scenarios related to AWS EC2** that are commonly asked in interviews.

---

# Scenario 1: Unable to SSH into EC2 Instance

### Problem
You cannot connect to an EC2 instance using SSH.

### Possible Causes

1. Security group does not allow port **22**
2. Incorrect key pair
3. Instance not running
4. Wrong username
5. Network ACL blocking traffic

### Solution

Check:

```
EC2 → Security Groups → Inbound Rules
Allow SSH (22) from your IP
```

Correct SSH command:

```
ssh -i key.pem ubuntu@public-ip
```

---

# Scenario 2: EC2 Instance Website Not Accessible

### Problem
Your application is running but the website is not accessible via browser.

### Possible Causes

- Port 80 or 443 not allowed in security group
- Web server not running
- Firewall blocking traffic

### Solution

Allow HTTP in security group:

```
Type: HTTP
Port: 80
Source: 0.0.0.0/0
```

Check web server:

```
systemctl status nginx
systemctl status apache2
```

---

# Scenario 3: EC2 Instance Disk Full

### Problem
Application stopped working because disk space is full.

### Check Disk Usage

```
df -h
```

Find large files:

```
du -ah | sort -rh | head
```

### Solution

- Delete unnecessary logs
- Clean temp files
- Extend EBS volume

Extend volume steps:

```
EC2 → Elastic Block Store → Volumes
Modify volume size
```

Then resize filesystem.

---

# Scenario 4: High CPU Usage on EC2

### Problem
CPU usage suddenly increased.

### Check CPU usage

```
top
```

or

```
htop
```

### Solution

- Identify high CPU process
- Restart application
- Scale instances using Auto Scaling

---

# Scenario 5: EC2 Instance Lost Public IP

### Problem
After stopping and starting the instance, the public IP changed.

### Cause

Public IP changes when instance stops.

### Solution

Use **Elastic IP**.

Steps:

```
EC2 → Elastic IPs → Allocate
Associate with instance
```

---

# Scenario 6: Application Down Because Instance Terminated

### Problem
Production instance terminated accidentally.

### Solution

Use:

- Auto Scaling Group
- Load Balancer

Auto Scaling will automatically launch new instances.

---

# Scenario 7: Application Cannot Connect to Database

### Problem
Backend application cannot connect to MySQL database.

### Possible Causes

- Database security group blocking port
- Wrong DB credentials
- Database service not running

### Solution

Allow database port:

```
MySQL → 3306
```

Check service:

```
systemctl status mysql
```

---

# Scenario 8: Slow Application Performance

### Problem
Users report slow response from application.

### Possible Causes

- Small instance type
- High CPU usage
- Insufficient memory

### Solution

Upgrade instance type.

Example:

```
t2.micro → t3.medium
```

---

# Scenario 9: Multiple EC2 Instances Needed for Traffic

### Problem
Single EC2 instance cannot handle high traffic.

### Solution

Use:

```
Application Load Balancer
Auto Scaling Group
```

Architecture:

```
Users
   ↓
Load Balancer
   ↓
Multiple EC2 Instances
```

---

# Scenario 10: Need Automatic Deployment on Instance Start

### Problem
You want application to install automatically when EC2 launches.

### Solution

Use **User Data Script**

Example:

```bash
#!/bin/bash
apt update -y
apt install nginx -y
systemctl start nginx
```

---

# Scenario 11: Instance Memory Issue

### Problem
Application crashes due to low memory.

### Check memory usage

```
free -m
```

### Solution

Upgrade instance type or optimize application.

---

# Scenario 12: Need Backup of EC2 Data

### Problem
You want automatic backups of instance data.

### Solution

Use **EBS Snapshots**.

Steps:

```
EC2 → Volumes → Create Snapshot
```

Or automate using **Lifecycle Manager**.

---

# Scenario 13: Instance Not Reachable After Deployment

### Problem
Instance is running but not reachable.

### Check

- Security group rules
- Route table
- Internet Gateway
- Instance status checks

---

# Scenario 14: Need High Availability

### Problem
Application should not go down if one instance fails.

### Solution

Use:

```
Load Balancer
Auto Scaling Group
Multiple Availability Zones
```

---

# Scenario 15: Need Cost Optimization

### Problem
Infrastructure cost is too high.

### Solution

Use:

- Spot instances
- Reserved instances
- Savings plans
- Auto scaling

---

# 🎯 Why DevOps Engineers Must Know EC2 Scenarios

DevOps engineers must troubleshoot issues like:

- Instance connectivity
- High CPU or memory usage
- Disk space problems
- Deployment failures
- Scaling infrastructure

These **real-world troubleshooting scenarios are very common in DevOps interviews.**
