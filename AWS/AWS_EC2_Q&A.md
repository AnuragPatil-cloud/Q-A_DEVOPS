# ☁ AWS EC2 Services Interview Questions & Answers (DevOps)

This section covers important **AWS EC2 services and components** commonly asked in DevOps interviews.

---

# 🚀 Instances

## 1. What is an EC2 Instance?

An EC2 instance is a **virtual server in AWS cloud used to run applications**.

It provides scalable computing capacity without managing physical hardware.

Example uses:
- Web servers
- Application servers
- CI/CD servers
- Microservices

---

# 🖥 Instance Types

## 2. What are Instance Types?

Instance types define the **CPU, memory, storage, and networking capacity** of an EC2 instance.

Examples:

| Type | Purpose |
|-----|--------|
t2/t3 | General purpose |
c5 | Compute optimized |
r5 | Memory optimized |
i3 | Storage optimized |

---

# 📦 Launch Templates

## 3. What is a Launch Template?

A Launch Template is a **configuration template used to launch EC2 instances**.

It contains:

- AMI ID
- Instance type
- Security groups
- Key pair
- User data

Launch templates are commonly used with **Auto Scaling Groups**.

---

# 💰 Spot Requests

## 4. What are Spot Instances?

Spot Instances allow you to **use unused AWS compute capacity at a lower cost**.

Advantages:

- Up to 90% cheaper
- Ideal for batch workloads

Disadvantage:

- Instances can be interrupted by AWS.

---

# 💳 Savings Plans

## 5. What is a Savings Plan?

Savings Plans provide **discounted pricing in exchange for a commitment to use AWS resources for 1–3 years**.

Benefits:

- Lower compute cost
- Flexible usage across instances

---

# 📅 Reserved Instances

## 6. What are Reserved Instances?

Reserved Instances allow users to **reserve EC2 capacity for 1 or 3 years to get significant discounts**.

Advantages:

- Lower cost
- Predictable usage

---

# 🏢 Dedicated Hosts

## 7. What are Dedicated Hosts?

Dedicated Hosts are **physical servers dedicated to a single customer**.

Used for:

- Compliance requirements
- Licensing restrictions

---

# 📌 Capacity Reservations

## 8. What are Capacity Reservations?

Capacity Reservations allow you to **reserve compute capacity in a specific Availability Zone**.

Benefits:

- Guaranteed capacity
- Useful for critical workloads

---

# 📊 Capacity Manager

## 9. What is Capacity Manager?

Capacity Manager helps manage **compute capacity across EC2 instances, reservations, and scaling resources**.

It helps optimize:

- resource allocation
- cost efficiency

---

# 🖼 Images

## 10. What are Images in EC2?

Images are **templates used to launch EC2 instances**.

Images include:

- Operating system
- Application configuration
- Software packages

---

# 📀 AMIs

## 11. What is an AMI?

AMI (Amazon Machine Image) is a **preconfigured template used to create EC2 instances**.

Example AMIs:

- Amazon Linux
- Ubuntu
- RedHat

---

# 📚 AMI Catalog

## 12. What is AMI Catalog?

AMI Catalog is a **central place to manage and discover approved AMIs within an organization**.

Benefits:

- Standardized images
- Improved security

---

# 💾 Elastic Block Store (EBS)

## 13. What is EBS?

EBS provides **persistent block storage for EC2 instances**.

Features:

- High availability
- Snapshot backups
- Persistent storage

---

# 📦 Volumes

## 14. What are EBS Volumes?

EBS volumes are **block storage devices attached to EC2 instances**.

Types:

- gp2/gp3 (General Purpose)
- io1/io2 (Provisioned IOPS)
- st1 (Throughput optimized)

---

# 📸 Snapshots

## 15. What are EBS Snapshots?

Snapshots are **backups of EBS volumes stored in S3**.

Benefits:

- Disaster recovery
- Data backup
- Volume restoration

---

# 🔄 Lifecycle Manager

## 16. What is EBS Lifecycle Manager?

Lifecycle Manager automates **creation and deletion of EBS snapshots**.

Benefits:

- Automated backups
- Reduced manual work

---

# 🌐 Network & Security

## 17. What is Network & Security in EC2?

Network and security services help control **traffic, connectivity, and protection of EC2 instances**.

Examples:

- Security groups
- Elastic IP
- Network interfaces

---

# 🔐 Security Groups

## 18. What are Security Groups?

Security groups act as **virtual firewalls for EC2 instances**.

They control:

- Inbound traffic
- Outbound traffic

Example rules:

```
Allow SSH (22)
Allow HTTP (80)
Allow HTTPS (443)
```

---

# 🌍 Elastic IP

## 19. What is an Elastic IP?

Elastic IP is a **static public IP address assigned to an EC2 instance**.

Benefits:

- Fixed IP
- Can be reassigned to another instance

---

# 🧩 Placement Groups

## 20. What are Placement Groups?

Placement Groups control **how EC2 instances are placed within AWS infrastructure**.

Types:

- Cluster
- Spread
- Partition

Used for **high performance or fault tolerance**.

---

# 🔑 Key Pairs

## 21. What are Key Pairs?

Key pairs are used to **securely connect to EC2 instances via SSH**.

Components:

- Public key (stored in AWS)
- Private key (kept by user)

Example:

```
ssh -i key.pem ubuntu@ec2-ip
```

---

# 🌐 Network Interfaces

## 22. What is a Network Interface?

A network interface (ENI) is a **virtual network card attached to an EC2 instance**.

It provides:

- Private IP
- Security group association
- Network connectivity

---

# ⚖ Load Balancing

## 23. What is Load Balancing?

Load balancing distributes incoming traffic across multiple servers.

Benefits:

- High availability
- Fault tolerance
- Better performance

---

# 🔁 Load Balancers

## 24. What are AWS Load Balancers?

Load balancers distribute traffic across multiple EC2 instances.

Types:

- Application Load Balancer (ALB)
- Network Load Balancer (NLB)
- Gateway Load Balancer

---

# 🎯 Target Groups

## 25. What is a Target Group?

Target groups contain **instances or services that receive traffic from a load balancer**.

Example:

```
ALB → Target Group → EC2 Instances
```

---

# 🔐 Trust Stores

## 26. What are Trust Stores?

Trust stores store **trusted certificates used for secure communication**.

They help ensure:

- SSL/TLS security
- Trusted certificate validation

---

# 📈 Auto Scaling

## 27. What is Auto Scaling?

Auto Scaling automatically **adds or removes EC2 instances based on demand**.

Benefits:

- High availability
- Cost optimization

---

# ⚙ Auto Scaling Groups

## 28. What is an Auto Scaling Group?

Auto Scaling Group (ASG) manages **a group of EC2 instances and ensures the desired number of instances are running**.

Example:

```
Minimum instances: 2
Desired instances: 3
Maximum instances: 6
```

If one instance fails → ASG launches a new instance automatically.

---

# 🚀 Why EC2 Services Are Important for DevOps

DevOps engineers use EC2 services to:

- Deploy scalable infrastructure
- Automate application hosting
- Manage compute resources
- Ensure high availability
- Optimize cost
