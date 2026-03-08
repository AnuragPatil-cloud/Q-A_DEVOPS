# 🔐 AWS IAM Scenario-Based Interview Questions (DevOps)

This section contains **real-world IAM scenarios** commonly faced by DevOps engineers.

---

# Scenario 1: User Cannot Access S3 Bucket

### Problem
A developer cannot access an S3 bucket even though they have an IAM user.

### Possible Causes

- IAM policy not attached
- Wrong permission in policy
- Bucket policy blocking access

### Solution

Check IAM permissions:

```
IAM → Users → Permissions
```

Attach required policy:

```
AmazonS3FullAccess
```

Or create a custom policy allowing S3 access.

---

# Scenario 2: EC2 Instance Cannot Access S3

### Problem
Application running on EC2 cannot access an S3 bucket.

### Cause

No IAM role attached to EC2 instance.

### Solution

Create IAM role:

```
IAM → Roles → Create Role → EC2
```

Attach policy:

```
AmazonS3FullAccess
```

Then attach role to EC2 instance.

---

# Scenario 3: AWS CLI Command Shows Access Denied

### Problem

Running AWS CLI command gives:

```
AccessDenied
```

### Cause

IAM user does not have required permissions.

### Solution

Check attached policies:

```
IAM → Users → Permissions
```

Add the required policy for the service.

---

# Scenario 4: Developer Needs Access to Only One Service

### Problem

Developer should access only **EC2**, not other AWS services.

### Solution

Create custom policy:

```
Allow → EC2 actions
Deny → other services
```

Attach policy to developer user.

---

# Scenario 5: Multiple Developers Need Same Permissions

### Problem

Several developers need the same permissions.

### Solution

Create IAM group:

```
Developers
```

Attach policy to the group and add users to it.

---

# Scenario 6: Credentials Accidentally Shared

### Problem

An IAM user's access keys were accidentally exposed.

### Solution

Immediately:

```
IAM → Users → Security Credentials
```

Deactivate or delete the compromised keys.

Create new access keys.

---

# Scenario 7: Restrict AWS Access by IP Address

### Problem

Users should access AWS only from office network.

### Solution

Create policy condition:

```json
"IpAddress": {
 "aws:SourceIp": "192.168.1.0/24"
}
```

Attach policy to the user or group.

---

# Scenario 8: Temporary Access Needed for External Contractor

### Problem

External contractor needs temporary AWS access.

### Solution

Create IAM role with limited permissions and allow the contractor to assume the role.

Avoid creating permanent IAM users.

---

# Scenario 9: EC2 Application Should Access DynamoDB

### Problem

Application running on EC2 needs access to DynamoDB.

### Solution

Create IAM role:

```
EC2 → DynamoDB access
```

Attach role to EC2 instance.

Do not store credentials inside application code.

---

# Scenario 10: Prevent Deleting Critical Resources

### Problem

You want to prevent users from deleting important resources.

### Solution

Create policy:

```
Deny → Delete actions
```

Example:

```
ec2:TerminateInstances
s3:DeleteBucket
```

Attach policy to users or groups.

---

# Scenario 11: Secure Root Account

### Problem

Root account should not be used for daily tasks.

### Solution

Best practices:

- Enable MFA
- Create IAM admin user
- Use IAM users instead of root login

---

# Scenario 12: Restrict IAM User Permissions

### Problem

User has too many permissions.

### Solution

Follow **least privilege principle**.

Remove unnecessary policies and assign only required permissions.

---

# 🎯 Why IAM Scenarios Are Important for DevOps

DevOps engineers must handle:

- access control
- security policies
- service permissions
- credential management
- secure infrastructure access

These IAM troubleshooting questions are **commonly asked in DevOps interviews.**
