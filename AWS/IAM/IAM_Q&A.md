# 🔐 AWS IAM Interview Questions & Answers

This section contains commonly asked **AWS IAM (Identity and Access Management) interview questions** for DevOps engineers.

---

# 1. What is AWS IAM?

IAM (Identity and Access Management) is a service used to **securely control access to AWS resources**.

Using IAM, administrators can:

- Create users
- Assign permissions
- Manage roles
- Control access to AWS services

---

# 2. What are the main components of IAM?

IAM consists of four main components:

| Component | Description |
|-----------|-------------|
Users | Individual identities created for people or applications |
Groups | Collection of IAM users with similar permissions |
Roles | Temporary permissions assigned to AWS services or users |
Policies | Permission rules that define access to resources |

---

# 3. What is an IAM User?

An IAM user is an **identity created in AWS representing a person or application** that needs access to AWS services.

Each user can have:

- Username
- Password
- Access keys

---

# 4. What is an IAM Group?

An IAM group is a **collection of IAM users**.

Permissions are assigned to the group, and all users in the group inherit those permissions.

Example groups:

```
Developers
DevOps
Administrators
```

---

# 5. What is an IAM Role?

An IAM role is a **set of permissions that can be assumed by users or AWS services**.

Roles provide **temporary security credentials**.

Example:

```
EC2 accessing S3 bucket
Lambda accessing DynamoDB
```

---

# 6. What is an IAM Policy?

An IAM policy is a **JSON document that defines permissions** for users, groups, or roles.

Policies specify:

- What actions are allowed
- Which resources can be accessed

Example policy:

```json
{
 "Version": "2012-10-17",
 "Statement": [
  {
   "Effect": "Allow",
   "Action": "s3:ListBucket",
   "Resource": "*"
  }
 ]
}
```

---

# 7. What are the types of IAM policies?

There are two types of policies:

1️⃣ Managed Policies  
2️⃣ Inline Policies

Managed policies are reusable across multiple users and roles.

---

# 8. What is the principle of least privilege?

The **principle of least privilege** means giving users only the permissions they need to perform their tasks.

This improves security by minimizing unnecessary access.

---

# 9. What is Multi-Factor Authentication (MFA) in IAM?

MFA adds an **extra layer of security** to AWS accounts.

Users must provide:

- Password
- One-time code from an authentication device

---

# 10. What are Access Keys?

Access keys are credentials used for **programmatic access to AWS services**.

They consist of:

```
Access Key ID
Secret Access Key
```

They are used with:

- AWS CLI
- SDK
- APIs

---

# 11. What is the root user in AWS?

The root user is the **original AWS account owner** created during account setup.

It has **full access to all AWS services**.

Best practice: avoid using the root user for daily operations.

---

# 12. What is an IAM permission boundary?

Permission boundaries define the **maximum permissions an IAM user or role can have**.

They act as a security control to restrict access.

---

# 13. What is a trust relationship in IAM?

A trust relationship defines **who is allowed to assume an IAM role**.

Example:

```
EC2 service allowed to assume a role
```

---

# 14. What is IAM Identity Center?

IAM Identity Center (formerly AWS SSO) allows **centralized access management for multiple AWS accounts**.

It supports:

- Single sign-on
- Role-based access
- Integration with corporate directories

---

# 15. What are IAM best practices?

Common IAM best practices include:

- Enable MFA
- Avoid using root user
- Use IAM roles instead of access keys
- Apply least privilege principle
- Rotate access keys regularly
- Use groups to manage permissions
