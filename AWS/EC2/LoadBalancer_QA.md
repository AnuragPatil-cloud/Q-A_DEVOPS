# ⚖ AWS Load Balancer Interview Questions & Scenarios

This section contains commonly asked **AWS Load Balancer interview questions and real DevOps troubleshooting scenarios**.

Load balancing helps distribute incoming traffic across multiple servers to ensure **high availability, scalability, and fault tolerance**.

---

# 🔹 Load Balancer Interview Questions

## 1. What is a Load Balancer?

A Load Balancer is a service that **distributes incoming traffic across multiple servers or instances**.

Benefits:

- High availability
- Fault tolerance
- Scalability
- Improved performance

---

## 2. What are the types of AWS Load Balancers?

AWS provides three types of load balancers:

| Load Balancer | Layer | Use Case |
|---|---|---|
Application Load Balancer (ALB) | Layer 7 | HTTP/HTTPS traffic |
Network Load Balancer (NLB) | Layer 4 | High-performance TCP/UDP traffic |
Gateway Load Balancer (GWLB) | Layer 3 | Network security appliances |

---

## 3. What is an Application Load Balancer (ALB)?

ALB works at **Layer 7 (Application Layer)** and routes traffic based on:

- URL path
- Hostname
- HTTP headers

Example:

```
example.com/login → Login service
example.com/products → Product service
```

---

## 4. What is a Network Load Balancer (NLB)?

NLB works at **Layer 4 (Transport Layer)** and handles:

- TCP
- UDP
- TLS traffic

It is designed for **high-performance applications requiring low latency**.

---

## 5. What is a Target Group?

A Target Group is a **group of resources that receive traffic from the load balancer**.

Targets can be:

- EC2 instances
- IP addresses
- Lambda functions

Architecture:

```
Load Balancer → Target Group → EC2 Instances
```

---

## 6. What is Health Check in Load Balancer?

Health checks monitor whether instances are **healthy and able to handle traffic**.

If an instance fails health checks:

- Load balancer stops sending traffic to it.

---

## 7. What is SSL Termination?

SSL termination allows the **load balancer to handle HTTPS encryption**.

Benefits:

- Offloads encryption work from servers
- Improves performance

---

## 8. What is Cross-Zone Load Balancing?

Cross-zone load balancing distributes traffic **across instances in multiple availability zones**.

This ensures better load distribution.

---

## 9. What is Sticky Session?

Sticky sessions ensure that **a user’s requests are always sent to the same backend server**.

Useful for applications requiring session persistence.

---

## 10. What is a Listener in Load Balancer?

A listener checks for incoming connection requests using a specific protocol and port.

Example:

```
HTTP : 80
HTTPS : 443
```

The listener forwards requests to the appropriate target group.

---

# 🔧 Real DevOps Load Balancer Scenarios

---

## Scenario 1: Website Not Accessible Through Load Balancer

### Problem

Users cannot access the website via the load balancer DNS.

### Possible Causes

- Security group blocking port
- Instances not healthy
- Web server not running

### Solution

Check:

```
EC2 → Target Groups → Health Status
```

Verify security group rules:

```
Allow HTTP (80)
Allow HTTPS (443)
```

---

## Scenario 2: Instances Showing Unhealthy

### Problem

All instances in target group show **unhealthy**.

### Cause

Health check configuration incorrect.

### Solution

Check health check path:

Example:

```
/health
/index.html
```

Also ensure application is running.

---

## Scenario 3: Traffic Going to Only One Instance

### Problem

Load is not distributed across instances.

### Possible Causes

- Sticky sessions enabled
- Only one healthy instance

### Solution

Check:

```
Target group → Healthy instances
```

Disable sticky sessions if unnecessary.

---

## Scenario 4: High Latency in Application

### Problem

Users report slow response times.

### Possible Causes

- Instance overloaded
- Insufficient instances

### Solution

Use:

```
Auto Scaling Group
```

Architecture:

```
Users
 ↓
Load Balancer
 ↓
Auto Scaling Group
 ↓
Multiple EC2 Instances
```

---

## Scenario 5: SSL Certificate Not Working

### Problem

HTTPS site shows certificate error.

### Cause

Certificate not attached to load balancer.

### Solution

Attach certificate using:

```
AWS Certificate Manager (ACM)
```

Then configure HTTPS listener.

---

## Scenario 6: Load Balancer Cannot Reach Instances

### Problem

Load balancer cannot communicate with EC2 instances.

### Cause

Security group rules blocking traffic.

### Solution

Allow traffic from load balancer security group.

Example:

```
Source: LoadBalancer-SG
Port: 80
```

---

## Scenario 7: Application Needs Zero Downtime Deployment

### Problem

Application updates cause downtime.

### Solution

Use load balancer with:

- multiple EC2 instances
- rolling deployments

Deployment flow:

```
Deploy new version
Health check passes
Traffic redirected
Old version removed
```

---

# 🎯 Why Load Balancer Knowledge is Important for DevOps

DevOps engineers must understand load balancing to ensure:

- high availability
- fault tolerance
- traffic distribution
- scalable architecture

Load balancers are widely used with:

- EC2
- Kubernetes
- Auto Scaling
- Microservices architectures
