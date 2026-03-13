# 🌐 AWS VPC Interview Questions & Answers

This section contains commonly asked **AWS VPC (Virtual Private Cloud) interview questions** for DevOps engineers.

---

# 1. What is a VPC?

A VPC (Virtual Private Cloud) is a **virtual network in AWS where you can launch AWS resources in a logically isolated environment**.

It allows you to control:

- IP address ranges
- subnets
- routing
- security

---

# 2. What are the main components of a VPC?

The main components of a VPC include:

- Subnets
- Route tables
- Internet Gateway
- NAT Gateway
- Security Groups
- Network ACLs
- Elastic IP

---

# 3. What is a Subnet?

A subnet is a **range of IP addresses within a VPC used to organize resources**.

Two types of subnets:

- Public Subnet
- Private Subnet

---

# 4. What is a Public Subnet?

A public subnet is a subnet where **instances can access the internet directly through an Internet Gateway**.

Example resources:

- web servers
- load balancers

---

# 5. What is a Private Subnet?

A private subnet is a subnet where **instances cannot access the internet directly**.

Example resources:

- databases
- internal application servers

---

# 6. What is an Internet Gateway?

An Internet Gateway (IGW) allows **communication between instances in a VPC and the internet**.

It is attached to the VPC.

---

# 7. What is a NAT Gateway?

A NAT Gateway allows **instances in a private subnet to access the internet without exposing them to incoming internet traffic**.

Example use case:

```
Private EC2 → NAT Gateway → Internet
```

---

# 8. What is a Route Table?

A route table contains **rules that determine how network traffic is directed inside a VPC**.

Example routes:

```
0.0.0.0/0 → Internet Gateway
```

---

# 9. What is CIDR in VPC?

CIDR (Classless Inter-Domain Routing) defines the **IP address range of the VPC**.

Example:

```
10.0.0.0/16
```

---

# 10. What is VPC Peering?

VPC peering allows **two VPCs to communicate with each other using private IP addresses**.

This enables resources in different VPCs to interact securely.

---

# 11. What is a Security Group?

A security group acts as a **virtual firewall for EC2 instances**.

It controls:

- inbound traffic
- outbound traffic

Security groups are **stateful**.

---

# 12. What is a Network ACL?

Network ACL (Access Control List) is a **firewall that controls traffic at the subnet level**.

Unlike security groups, network ACLs are **stateless**.

---

# 13. What is the difference between Security Group and NACL?

| Feature | Security Group | NACL |
|---|---|---|
Level | Instance level | Subnet level |
State | Stateful | Stateless |
Rules | Allow only | Allow and Deny |

---

# 14. What is an Elastic IP?

An Elastic IP is a **static public IP address used for AWS resources such as EC2 instances**.

It remains constant even if the instance is restarted.

---

# 15. What is VPC Endpoint?

A VPC endpoint allows **private communication between a VPC and AWS services without using the internet**.

Example services:

- S3
- DynamoDB

---

# 16. What is VPC Flow Log?

VPC Flow Logs capture **information about IP traffic going to and from network interfaces in a VPC**.

It helps with:

- monitoring
- troubleshooting
- security analysis

---

# 17. What is a Bastion Host?

A Bastion Host is an **EC2 instance in a public subnet used to securely access instances in private subnets via SSH**.

Architecture example:

```
Admin → Bastion Host → Private EC2
```

---

# 18. What is VPC CIDR Block?

The CIDR block defines the **IP address range available for the VPC**.

Example:

```
10.0.0.0/16
```

This range can be divided into smaller subnet ranges.

---

# 19. What is AWS Transit Gateway?

Transit Gateway allows **multiple VPCs and on-premise networks to connect through a central hub**.

It simplifies network architecture.

---

# 20. Why is VPC important for DevOps?

VPC is important because it provides:

- network isolation
- secure infrastructure
- controlled access to resources
- scalable cloud networking
