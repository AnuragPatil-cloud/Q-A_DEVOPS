# 📦 Amazon S3 Scenario-Based DevOps Interview Questions

This section contains **real-world troubleshooting scenarios related to Amazon S3** commonly faced by DevOps engineers.

---

# Scenario 1: Access Denied When Accessing S3 Bucket

### Problem
User gets the error:

```
AccessDenied
```

when trying to access an S3 bucket.

### Possible Causes

- IAM user does not have permission
- Bucket policy blocking access
- Public access blocked

### Solution

Check:

```
IAM → User → Permissions
```

Verify bucket policy:

```
S3 → Bucket → Permissions → Bucket Policy
```

Ensure required permissions like:

```
s3:GetObject
s3:ListBucket
```

---

# Scenario 2: Unable to Upload Files to S3

### Problem
Application cannot upload files to an S3 bucket.

### Possible Causes

- Missing IAM permissions
- Bucket policy restrictions
- Incorrect credentials

### Solution

Ensure IAM role or user has permissions:

```
s3:PutObject
```

Verify bucket permissions and credentials.

---

# Scenario 3: S3 Static Website Not Loading

### Problem
Static website hosted on S3 shows:

```
Access Denied
```

### Possible Causes

- Bucket not public
- Incorrect bucket policy
- Static hosting not enabled

### Solution

Enable static hosting:

```
S3 → Bucket → Properties → Static Website Hosting
```

Update bucket policy to allow public read access.

---

# Scenario 4: Objects Not Replicating Between Buckets

### Problem
Cross-region replication not working.

### Possible Causes

- Versioning not enabled
- Incorrect IAM role
- Replication rule misconfigured

### Solution

Ensure:

```
Versioning enabled on both buckets
```

Check replication configuration and IAM role permissions.

---

# Scenario 5: Large File Upload Fails

### Problem
Uploading large files fails or is slow.

### Cause

Single upload request.

### Solution

Use **Multipart Upload**.

This splits the file into multiple parts and uploads them in parallel.

---

# Scenario 6: Terraform State File Accidentally Deleted

### Problem
Terraform state file stored in S3 was deleted.

### Solution

Enable **versioning on the S3 bucket**.

Then restore previous version of the state file.

---

# Scenario 7: Application Cannot Access S3 from EC2

### Problem
Application running on EC2 cannot access S3.

### Cause

EC2 instance has no IAM role.

### Solution

Create IAM role with S3 permissions and attach it to the EC2 instance.

---

# Scenario 8: S3 Storage Cost Increasing

### Problem
S3 storage cost is very high.

### Cause

Old files stored in S3 Standard.

### Solution

Use **Lifecycle policies**.

Example:

```
Move files to Glacier after 30 days
```

This reduces storage cost.

---

# Scenario 9: Public Files Accidentally Exposed

### Problem
Sensitive data stored in S3 became publicly accessible.

### Solution

Enable **Block Public Access**.

Steps:

```
S3 → Bucket → Permissions → Block Public Access
```

Remove public policies and restrict access using IAM.

---

# Scenario 10: Logs Not Appearing in S3 Bucket

### Problem
Application logs expected in S3 are missing.

### Possible Causes

- Logging not enabled
- Wrong bucket configured
- Permission issue

### Solution

Check logging configuration and ensure correct bucket and IAM permissions.

---

# 🎯 Why S3 Scenarios Are Important for DevOps

DevOps engineers must troubleshoot issues like:

- access permission errors
- storage cost optimization
- backup and recovery
- static website hosting problems
- replication failures

Understanding these scenarios helps maintain **secure and reliable storage infrastructure**.
