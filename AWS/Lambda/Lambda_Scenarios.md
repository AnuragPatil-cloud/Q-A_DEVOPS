# ⚡ AWS Lambda Scenario-Based DevOps Interview Questions

This section contains **real-world AWS Lambda troubleshooting scenarios** commonly faced by DevOps engineers.

---

# Scenario 1: Lambda Function Not Triggering from S3

### Problem
A file is uploaded to an S3 bucket but the Lambda function is not triggered.

### Possible Causes

- S3 event notification not configured
- Lambda permission missing
- Incorrect bucket or prefix configuration

### Solution

Check:

```
S3 → Properties → Event Notifications
```

Ensure:

- Correct Lambda function selected
- Correct event type (PUT, POST, etc.)

Also verify Lambda permission:

```
Lambda → Permissions → Resource Policy
```

---

# Scenario 2: Lambda Function Timeout Error

### Problem

Lambda function fails with error:

```
Task timed out
```

### Possible Causes

- Long-running process
- Slow external API
- Large file processing

### Solution

Increase timeout setting:

```
Lambda → Configuration → General Configuration → Timeout
```

Maximum timeout:

```
15 minutes
```

Also optimize the function code.

---

# Scenario 3: Lambda Permission Denied to Access S3

### Problem

Lambda function cannot read from an S3 bucket.

### Cause

Lambda execution role lacks S3 permissions.

### Solution

Attach policy to Lambda role:

```
AmazonS3FullAccess
```

Or create a custom policy allowing:

```
s3:GetObject
s3:PutObject
```

---

# Scenario 4: Lambda Function Not Logging

### Problem

No logs are appearing in CloudWatch.

### Cause

Lambda execution role lacks logging permissions.

### Solution

Attach policy:

```
AWSLambdaBasicExecutionRole
```

This allows Lambda to write logs to CloudWatch.

---

# Scenario 5: Lambda Cold Start Issue

### Problem

First request to Lambda takes longer than expected.

### Cause

Cold start occurs when Lambda initializes a new execution environment.

### Solution

Options:

- Increase memory allocation
- Use Provisioned Concurrency
- Reduce initialization code

---

# Scenario 6: Lambda Cannot Connect to Database

### Problem

Lambda cannot connect to a database hosted in a VPC.

### Cause

Lambda function not configured inside the VPC.

### Solution

Configure Lambda VPC settings:

```
Lambda → Configuration → VPC
```

Select:

- Correct VPC
- Subnets
- Security groups

---

# Scenario 7: Lambda Deployment Package Too Large

### Problem

Deployment fails due to package size.

### Cause

Lambda has size limits.

Limits:

```
ZIP upload limit: 50 MB
Uncompressed limit: 250 MB
```

### Solution

Use:

```
Lambda Layers
```

Or store dependencies in layers.

---

# Scenario 8: Lambda Function Running Multiple Times

### Problem

Lambda function executes multiple times unexpectedly.

### Cause

Retry behavior from event source.

Example:

- SQS
- SNS
- EventBridge

### Solution

Check event source retry configuration.

Configure **Dead Letter Queue (DLQ)** to handle failures.

---

# Scenario 9: Lambda Function Memory Issue

### Problem

Lambda function fails due to insufficient memory.

### Cause

Memory allocation too low.

### Solution

Increase memory:

```
Lambda → Configuration → Memory
```

Increasing memory also increases CPU performance.

---

# Scenario 10: Lambda Function Cannot Access DynamoDB

### Problem

Lambda application cannot read/write DynamoDB.

### Cause

Missing IAM permissions.

### Solution

Attach policy:

```
AmazonDynamoDBFullAccess
```

Or allow specific actions:

```
dynamodb:GetItem
dynamodb:PutItem
```

---

# Scenario 11: Lambda Triggered Too Frequently

### Problem

Lambda execution cost increases due to too many invocations.

### Cause

Event trigger firing too often.

### Solution

Optimize triggers:

- Use filters
- Reduce event frequency
- Use batching where possible

---

# Scenario 12: Lambda Function Fails After Deployment

### Problem

Function fails immediately after deployment.

### Possible Causes

- Missing dependencies
- Incorrect runtime
- Wrong environment variables

### Solution

Check:

```
CloudWatch Logs
```

Verify:

- runtime configuration
- dependencies included
- environment variables

---

# 🎯 Why Lambda Scenarios Are Important for DevOps

DevOps engineers must troubleshoot issues such as:

- permission errors
- event trigger failures
- cold start delays
- deployment problems
- scaling issues

Understanding these scenarios helps ensure **reliable serverless applications in production environments**.
