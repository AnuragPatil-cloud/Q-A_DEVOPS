# ☁ AWS Interview Questions & Answers (DevOps)

This section contains commonly asked **AWS interview questions for DevOps Engineers (Fresher – 2+ Years Experience).**

---

# 1. What is AWS?

AWS (Amazon Web Services) is a **cloud computing platform provided by Amazon** that offers services like computing, storage, networking, databases, and more.

It allows users to run applications without managing physical servers.

---

# 2. What are the main benefits of AWS?

- Scalability
- High availability
- Pay-as-you-go pricing
- Global infrastructure
- Security

---

# 3. What are the main AWS service categories?

- Compute
- Storage
- Networking
- Database
- Security
- Monitoring

---

# 4. What is Amazon EC2?

EC2 (Elastic Compute Cloud) is a **virtual server in the cloud** used to run applications.

Features:

- Different instance types
- Auto scaling
- Elastic IP
- Security groups

---

# 5. What is Amazon S3?

S3 (Simple Storage Service) is an **object storage service used to store files, backups, and static content.**

Features:

- High durability
- Scalable storage
- Versioning
- Lifecycle policies

---

# 6. What is a VPC?

VPC (Virtual Private Cloud) is a **virtual network in AWS where you can launch resources securely.**

It allows you to control:

- IP address range
- Subnets
- Route tables
- Internet gateways

---

# 7. What are Subnets?

Subnets are **segments of a VPC network** used to organize resources.

Types:

Public Subnet  
Resources have internet access.

Private Subnet  
Resources do not have direct internet access.

---

# 8. What is an Internet Gateway?

An Internet Gateway allows **communication between a VPC and the internet.**

---

# 9. What is a NAT Gateway?

NAT Gateway allows **instances in a private subnet to access the internet without exposing them to incoming traffic.**

---

# 10. What are Security Groups?

Security groups act as **virtual firewalls for EC2 instances**.

They control:

- Inbound traffic
- Outbound traffic

Example rules:

- Allow SSH (22)
- Allow HTTP (80)

---

# 11. What is IAM?

IAM (Identity and Access Management) is used to **manage access to AWS services and resources.**

IAM components:

- Users
- Groups
- Roles
- Policies

---

# 12. What is an IAM Role?

An IAM role provides **temporary permissions to AWS services or users**.

Example:

EC2 instance accessing S3 bucket.

---

# 13. What is Auto Scaling?

Auto Scaling automatically **adjusts the number of EC2 instances based on demand**.

Benefits:

- High availability
- Cost optimization

---

# 14. What is Elastic Load Balancer (ELB)?

ELB distributes incoming traffic across multiple EC2 instances.

Types:

- Application Load Balancer (ALB)
- Network Load Balancer (NLB)
- Classic Load Balancer

---

# 15. What is Amazon RDS?

RDS (Relational Database Service) is a **managed database service**.

Supported databases:

- MySQL
- PostgreSQL
- MariaDB
- Oracle
- SQL Server

---

# 16. What is Amazon EBS?

EBS (Elastic Block Store) provides **persistent block storage for EC2 instances.**

Features:

- High performance
- Snapshot backups

---

# 17. What is Amazon EKS?

EKS (Elastic Kubernetes Service) is a **managed Kubernetes service in AWS.**

It allows running Kubernetes clusters without managing control plane infrastructure.

---

# 18. What is CloudWatch?

CloudWatch is a **monitoring service used to track AWS resources and applications.**

It provides:

- Metrics
- Logs
- Alarms

---

# 19. What is AWS CloudFormation?

CloudFormation is an **Infrastructure as Code service used to provision AWS resources using templates.**

---

# 20. What is the AWS Shared Responsibility Model?

AWS and the customer share security responsibilities.

AWS is responsible for:

- Physical data centers
- Hardware
- Network infrastructure

Customer is responsible for:

- Operating systems
- Applications
- Data security
- Access management

---

# 21. What are Availability Zones?

Availability Zones are **isolated data centers within an AWS region**.

They provide **high availability and fault tolerance**.

---

# 22. What is an AWS Region?

A region is a **geographic area where AWS data centers are located**.

Example:

- us-east-1
- ap-south-1

---

# 23. What is Route 53?

Route 53 is an **AWS DNS service used to route traffic to applications.**

Features:

- Domain registration
- Health checks
- Traffic routing

---

# 24. What is AWS Lambda?

Lambda is a **serverless compute service** that runs code without managing servers.

It executes code based on events.

---

# 25. Real DevOps AWS Scenario

### Problem

Application traffic increases suddenly.

### Solution

Use:

- Auto Scaling
- Load Balancer

This ensures:

- High availability
- Automatic scaling

---

# 🚀 Why AWS is Important for DevOps

AWS helps DevOps teams:

- Deploy scalable infrastructure
- Automate infrastructure
- Monitor applications
- Build CI/CD pipelines

AWS integrates with:

- Docker
- Kubernetes
- Terraform
- Jenkins
- GitHub Actions
