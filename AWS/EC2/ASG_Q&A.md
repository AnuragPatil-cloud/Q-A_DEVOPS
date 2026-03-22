# 📈 AWS Auto Scaling Group (ASG) Interview Questions & Answers (DevOps)

This section contains commonly asked **AWS Auto Scaling Group (ASG) interview questions** for DevOps engineers.

---

# 1. What is Auto Scaling in AWS?

Auto Scaling is a service that **automatically adjusts the number of EC2 instances based on traffic or demand**.

It helps maintain performance and optimize cost.

---

# 2. What is an Auto Scaling Group (ASG)?

An Auto Scaling Group is a **collection of EC2 instances managed together for automatic scaling and high availability**.

---

# 3. What are the main components of ASG?

Key components include:

- Launch Template / Launch Configuration
- Auto Scaling Group
- Scaling Policies
- CloudWatch Alarms

---

# 4. What is a Launch Template?

A Launch Template defines **configuration for EC2 instances**, such as:

- AMI
- instance type
- security groups
- key pair

---

# 5. What is the difference between Launch Template and Launch Configuration?

| Launch Template | Launch Configuration |
|---|---|
Latest version | Older version |
Supports versioning | No versioning |
More features | Limited features |

---

# 6. What is desired capacity in ASG?

Desired capacity is the **number of instances you want running in the group**.

---

# 7. What is minimum and maximum capacity?

- Minimum: minimum number of instances
- Maximum: maximum number of instances allowed

Example:

```
Min: 2
Max: 10
Desired: 4
```

---

# 8. What are scaling policies?

Scaling policies define **how ASG scales instances up or down**.

Types:

- Target tracking scaling
- Step scaling
- Simple scaling

---

# 9. What is Target Tracking Scaling?

Automatically adjusts capacity to **maintain a specific metric value**.

Example:

```
CPU utilization = 50%
```

---

# 10. What is Step Scaling?

Scaling happens in **steps based on metric thresholds**.

Example:

```
CPU > 70% → add 2 instances
CPU > 90% → add 4 instances
```

---

# 11. What is Simple Scaling?

Simple scaling triggers **one scaling action at a time with cooldown period**.

---

# 12. What is Cooldown Period?

Cooldown is the **time ASG waits before performing another scaling action**.

---

# 13. What is Health Check in ASG?

ASG checks whether instances are healthy.

Types:

- EC2 health check
- ELB health check

Unhealthy instances are replaced automatically.

---

# 14. What is Lifecycle Hook?

Lifecycle hooks allow **custom actions during instance launch or termination**.

Example:

- run scripts before instance termination

---

# 15. What is Scaling Out and Scaling In?

- Scaling Out → adding instances
- Scaling In → removing instances

---

# 16. What is Elastic Load Balancer with ASG?

ASG works with load balancers to:

- distribute traffic
- maintain high availability

---

# 17. What is Multi-AZ deployment in ASG?

ASG can launch instances across **multiple availability zones for high availability**.

---

# 18. What is termination policy in ASG?

Termination policy defines **which instance to terminate during scale-in**.

---

# 19. What are common use cases of ASG?

- handling traffic spikes
- cost optimization
- high availability
- fault tolerance

---

# 20. Why is ASG important for DevOps?

ASG helps DevOps teams:

- automate scaling
- improve application availability
- reduce manual intervention
- optimize cloud cost
