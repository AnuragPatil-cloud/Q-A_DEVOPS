# 🗄 Amazon RDS Scenario-Based DevOps Interview Questions

This section contains **real-world Amazon RDS troubleshooting scenarios** commonly faced by DevOps engineers.

---

# Scenario 1: Application Cannot Connect to RDS

### Problem
Application cannot connect to the RDS database.

### Possible Causes

- Security group blocking traffic
- Incorrect database endpoint
- Database instance not running
- Wrong credentials

### Solution

Check security group rules:

```
Allow port 3306 (MySQL)
Allow port 5432 (PostgreSQL)
```

Verify endpoint and credentials.

Check database status in AWS console.

---

# Scenario 2: RDS Database Connection Timeout

### Problem
Application shows connection timeout when connecting to RDS.

### Possible Causes

- RDS instance inside private subnet
- Security group not allowing inbound traffic
- Network configuration issue

### Solution

Verify:

```
RDS security group rules
VPC routing configuration
Application network access
```

Ensure application server can reach the RDS instance.

---

# Scenario 3: High CPU Usage in RDS

### Problem
Database performance is slow due to high CPU usage.

### Possible Causes

- inefficient queries
- high traffic
- insufficient instance size

### Solution

Use:

```
CloudWatch metrics
Performance Insights
```

Optimize queries or upgrade instance type.

---

# Scenario 4: RDS Storage Almost Full

### Problem
Database storage is reaching maximum capacity.

### Solution

Enable **storage autoscaling** or manually increase storage size.

Steps:

```
RDS → Modify Instance → Increase Storage
```

---

# Scenario 5: Need High Availability for Database

### Problem
Database should remain available even if one AZ fails.

### Solution

Enable **Multi-AZ deployment**.

This creates a standby replica in another availability zone and enables automatic failover.

---

# Scenario 6: Read Performance is Slow

### Problem
Application has many read requests and database performance decreases.

### Solution

Create **Read Replicas**.

Architecture:

```
Application
     ↓
Primary DB
     ↓
Read Replica
```

Read queries can be distributed across replicas.

---

# Scenario 7: RDS Snapshot Needed for Backup

### Problem
You need to create a manual backup before deploying major changes.

### Solution

Create a snapshot:

```
RDS → Snapshots → Create Snapshot
```

Snapshots allow restoring database if deployment fails.

---

# Scenario 8: RDS Instance Accidentally Deleted

### Problem
Database instance was accidentally deleted.

### Solution

Restore from backup or snapshot:

```
RDS → Snapshots → Restore DB Instance
```

---

# Scenario 9: Database Upgrade Required

### Problem
Database version needs to be upgraded.

### Solution

Use RDS upgrade option:

```
RDS → Modify Instance → Engine Version
```

Perform upgrade during maintenance window.

---

# Scenario 10: Application Cannot Access RDS in Private Subnet

### Problem
Application cannot reach RDS instance deployed in a private subnet.

### Possible Causes

- Application server in different subnet
- Security group restrictions
- VPC configuration issue

### Solution

Ensure:

- both resources are in same VPC
- security group allows database port
- routing is configured correctly

---

# 🎯 Why RDS Scenarios Are Important for DevOps

DevOps engineers must troubleshoot:

- database connectivity issues
- performance problems
- storage limitations
- failover and backup strategies

Understanding these scenarios helps maintain **reliable and scalable database infrastructure**.
