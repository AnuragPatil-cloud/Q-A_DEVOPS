# 📦 Amazon S3 Interview Questions & Answers

This section contains commonly asked **Amazon S3 (Simple Storage Service) interview questions** for DevOps engineers.

---

# 1. What is Amazon S3?

Amazon S3 (Simple Storage Service) is an **object storage service provided by AWS used to store and retrieve data from anywhere on the internet**.

It provides:

- high durability
- scalability
- high availability

---

# 2. What is an S3 Bucket?

An S3 bucket is a **container used to store objects (files) in Amazon S3**.

Example:

```
my-backup-bucket
company-data-bucket
```

Each bucket name must be **globally unique**.

---

# 3. What is an Object in S3?

An object is the **actual file stored inside an S3 bucket**.

Each object contains:

- data (file)
- metadata
- unique key

Example:

```
image.jpg
backup.zip
logs.txt
```

---

# 4. What are S3 Storage Classes?

S3 provides multiple storage classes for different use cases.

| Storage Class | Use Case |
|---|---|
S3 Standard | Frequently accessed data |
S3 Standard-IA | Infrequent access data |
S3 One Zone-IA | Lower-cost infrequent access |
S3 Glacier | Archival storage |
S3 Glacier Deep Archive | Long-term archival |

---

# 5. What is S3 Versioning?

Versioning allows **multiple versions of the same object to be stored in a bucket**.

Benefits:

- protects against accidental deletion
- allows recovery of previous versions

---

# 6. What is S3 Lifecycle Policy?

Lifecycle policies automatically **move or delete objects based on predefined rules**.

Example:

```
Move files to Glacier after 30 days
Delete files after 1 year
```

---

# 7. What is S3 Bucket Policy?

A bucket policy is a **JSON-based access control policy applied to an S3 bucket**.

It defines:

- who can access the bucket
- what actions are allowed

---

# 8. What is the difference between Bucket Policy and IAM Policy?

| IAM Policy | Bucket Policy |
|---|---|
Attached to users, groups, or roles | Attached directly to the bucket |
Controls user permissions | Controls bucket access |

---

# 9. What is S3 Object Encryption?

Encryption protects data stored in S3.

Types of encryption:

- SSE-S3 (AWS managed keys)
- SSE-KMS (KMS managed keys)
- SSE-C (Customer managed keys)

---

# 10. What is S3 Pre-signed URL?

A pre-signed URL allows **temporary access to a private S3 object**.

It is commonly used to:

- upload files
- download files securely

---

# 11. What is S3 Static Website Hosting?

S3 can host **static websites**.

It supports files such as:

```
HTML
CSS
JavaScript
Images
```

Example:

```
index.html
error.html
```

---

# 12. What is S3 Cross-Region Replication?

Cross-region replication automatically **copies objects from one S3 bucket to another bucket in a different region**.

Benefits:

- disaster recovery
- high availability

---

# 13. What is S3 Event Notification?

S3 can trigger events when objects change.

Example triggers:

- file upload
- file deletion

These events can trigger:

- AWS Lambda
- SNS
- SQS

---

# 14. What is S3 Transfer Acceleration?

Transfer acceleration speeds up **file uploads to S3 using AWS edge locations**.

Useful for:

- global users
- large file uploads

---

# 15. What is S3 Durability?

Amazon S3 provides **99.999999999% (11 nines) durability**.

This means data is highly protected against loss.

---

# 16. What is S3 Consistency Model?

Amazon S3 provides:

- **strong read-after-write consistency**
- immediate availability of new objects after upload

---

# 17. What is Multipart Upload in S3?

Multipart upload allows **large files to be uploaded in smaller parts simultaneously**.

Benefits:

- faster uploads
- better reliability

---

# 18. What are common use cases of S3?

Common S3 use cases include:

- data backup
- log storage
- static website hosting
- big data storage
- media storage

---

# 19. What is S3 Access Control List (ACL)?

ACL is a **legacy access control method used to grant permissions to objects and buckets**.

Modern best practice is to use:

```
IAM policies
Bucket policies
```

---

# 20. Why is Amazon S3 important for DevOps?

S3 is widely used by DevOps engineers for:

- storing application backups
- storing logs
- hosting static websites
- Terraform state storage
- artifact storage in CI/CD pipelines
