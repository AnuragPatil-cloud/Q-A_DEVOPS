# 🗄 Amazon RDS Interview Questions & Answers

This section contains commonly asked **Amazon RDS (Relational Database Service) interview questions** for DevOps engineers.

---

# 1. What is Amazon RDS?

Amazon RDS (Relational Database Service) is a **managed database service provided by AWS that makes it easy to set up, operate, and scale relational databases in the cloud**.

AWS handles:

- database setup
- backups
- patching
- scaling
- maintenance

---

# 2. What databases are supported by Amazon RDS?

Amazon RDS supports multiple relational databases such as:

- MySQL
- PostgreSQL
- MariaDB
- Oracle
- Microsoft SQL Server
- Amazon Aurora

---

# 3. What is a DB Instance in RDS?

A DB instance is a **database environment running in the AWS cloud**.

It contains:

- database engine
- compute resources
- storage
- memory

---

# 4. What is Amazon Aurora?

Amazon Aurora is a **high-performance relational database engine compatible with MySQL and PostgreSQL**.

It provides:

- higher performance
- better scalability
- automatic replication

---

# 5. What is Multi-AZ deployment in RDS?

Multi-AZ deployment creates **a standby replica in another availability zone for high availability**.

If the primary database fails, AWS automatically switches to the standby instance.

---

# 6. What is Read Replica in RDS?

Read replicas are **copies of a database used to improve read performance**.

They are used for:

- read-heavy workloads
- scaling database reads

---

# 7. What is automated backup in RDS?

RDS automatically creates **daily backups of the database and transaction logs**.

This allows restoring the database to a specific point in time.

---

# 8. What are RDS Snapshots?

Snapshots are **manual backups of RDS databases stored in S3**.

They can be used to:

- restore databases
- create new database instances

---

# 9. What is RDS storage scaling?

RDS allows **automatic storage scaling** when database storage usage increases.

This prevents database downtime due to storage limits.

---

# 10. What is RDS endpoint?

An endpoint is the **connection URL used by applications to connect to the RDS database**.

Example:

```
mydatabase.abc123.us-east-1.rds.amazonaws.com
```

---

# 11. What is RDS security?

RDS security is managed using:

- VPC
- security groups
- IAM authentication
- encryption

This ensures secure access to databases.

---

# 12. What is encryption in RDS?

Encryption protects database data using **AWS Key Management Service (KMS)**.

Encryption can be applied to:

- database storage
- backups
- snapshots

---

# 13. What is RDS maintenance window?

The maintenance window is a **scheduled time when AWS performs updates such as patching or upgrades**.

This helps ensure database stability.

---

# 14. What is the difference between Multi-AZ and Read Replica?

| Feature | Multi-AZ | Read Replica |
|---|---|---|
Purpose | High availability | Read scaling |
Replication | Synchronous | Asynchronous |
Failover | Automatic | Manual |

---

# 15. What is RDS parameter group?

A parameter group is a **collection of database configuration settings**.

It allows customization of database engine behavior.

---

# 16. What is RDS subnet group?

An RDS subnet group defines **which subnets inside a VPC can host RDS database instances**.

This ensures proper networking setup.

---

# 17. What is the difference between RDS and DynamoDB?

| Feature | RDS | DynamoDB |
|---|---|---|
Database Type | Relational | NoSQL |
Schema | Fixed schema | Flexible schema |
Use Case | Structured data | Large-scale applications |

---

# 18. What monitoring tools are used for RDS?

RDS can be monitored using:

- Amazon CloudWatch
- Enhanced monitoring
- Performance Insights

---

# 19. What are common use cases of RDS?

Common RDS use cases include:

- web applications
- enterprise applications
- e-commerce platforms
- CRM systems
- financial applications

---

# 20. Why is Amazon RDS important for DevOps?

Amazon RDS helps DevOps teams by:

- automating database management
- improving scalability
- ensuring high availability
- reducing operational overhead
