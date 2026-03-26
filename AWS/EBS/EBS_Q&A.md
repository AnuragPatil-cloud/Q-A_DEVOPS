# 💾 AWS EBS (Elastic Block Store) Interview Questions & Answers (DevOps)

This section contains **in-depth AWS EBS Q&A with real DevOps usage and practical explanations**.

---

# 1. What is AWS EBS?

## Answer
AWS EBS (Elastic Block Store) is a **block storage service used to provide persistent storage for EC2 instances**.

## Real DevOps Usage
👉 Used for:
- storing application data
- database storage
- OS disks for EC2

---

# 2. What is the difference between EBS and S3?

| Feature | EBS | S3 |
|---|---|---|
Type | Block storage | Object storage |
Usage | EC2 disks | File storage |
Access | Single instance | Multiple access |

## DevOps Usage
👉 EBS → database / OS  
👉 S3 → backups / logs  

---

# 3. What are EBS Volume Types?

## Answer

- gp2 / gp3 → General Purpose (most used)
- io1 / io2 → High performance (databases)
- st1 → Throughput optimized
- sc1 → Cold storage

## DevOps Usage
👉 gp3 → default for apps  
👉 io2 → high IOPS DB  

---

# 4. What is an EBS Snapshot?

## Answer
Snapshot is a **backup of an EBS volume stored in S3**.

## DevOps Usage
👉 Used for:
- backups
- disaster recovery
- creating new volumes

---

# 5. Can we attach multiple EBS volumes to one EC2?

## Answer
Yes, multiple EBS volumes can be attached to a single EC2 instance.

---

# 6. Can we attach one EBS volume to multiple EC2 instances?

## Answer
Generally no, except for **EBS Multi-Attach (io1/io2 volumes only)**.

---

# 7. What is EBS Multi-Attach?

## Answer
Allows a single EBS volume to be attached to **multiple EC2 instances simultaneously**.

## DevOps Usage
👉 Used in clustered applications.

---

# 8. What is the difference between EBS and Instance Store?

| Feature | EBS | Instance Store |
|---|---|---|
Persistence | Persistent | Temporary |
Data retention | Survives stop/start | Lost on stop |

## DevOps Usage
👉 Instance store → cache  
👉 EBS → important data  

---

# 9. What happens to EBS when EC2 is stopped?

## Answer
EBS volume **remains intact**.

---

# 10. What is Delete on Termination?

## Answer
Defines whether EBS volume is deleted when EC2 is terminated.

## DevOps Usage
👉 Disable for important data  

---

# 11. What is Encryption in EBS?

## Answer
EBS supports **encryption using AWS KMS**.

## DevOps Usage
👉 Used for:
- securing sensitive data
- compliance requirements  

---

# 12. What is IOPS in EBS?

## Answer
IOPS = Input/Output operations per second.

## DevOps Usage
👉 Important for:
- databases
- high-performance apps  

---

# 13. Can we resize EBS volume?

## Answer
Yes, EBS volumes can be resized dynamically.

## DevOps Usage
👉 Used when disk space increases in production.

---

# 14. What is EBS Optimization?

## Answer
Provides **dedicated bandwidth between EC2 and EBS**.

---

# 15. What is a Root Volume?

## Answer
The root volume contains the **OS of EC2 instance**.

---

# 16. What is Volume Attachment?

## Answer
Attaching EBS to EC2 to use it as storage.

---

# 17. What is Snapshot Lifecycle Policy?

## Answer
Automatically manages snapshots.

## DevOps Usage
👉 Used for:
- automated backups
- retention policies  

---

# 18. What is the difference between gp2 and gp3?

| Feature | gp2 | gp3 |
|---|---|---|
Performance | Linked to size | Independent |
Cost | Higher | Cheaper |

## DevOps Usage
👉 gp3 preferred in production  

---

# 19. What are common EBS use cases?

- databases
- application storage
- backups
- logs

---

# 20. Why is EBS important for DevOps?

EBS helps:

- store persistent data  
- support scalable infrastructure  
- enable backup and recovery  
- ensure data durability  

---

# 🎯 Interview Tip

If asked:

👉 “How do you use EBS in your project?”

Say:

- Used EBS for EC2 storage  
- Took snapshots for backup  
- Increased volume size when needed  
- Used encryption for security  
- Used gp3 for cost optimization  

---

# 🚀 Why This Section is Important

This shows:

✅ AWS storage knowledge  
✅ Real usage understanding  
✅ Production-level thinking  
