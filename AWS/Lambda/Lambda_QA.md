# ⚡ AWS Lambda Interview Questions & Answers

This section contains commonly asked **AWS Lambda interview questions** for DevOps engineers.

---

# 1. What is AWS Lambda?

AWS Lambda is a **serverless compute service that allows you to run code without managing servers**.

Lambda automatically handles:

- server provisioning
- scaling
- monitoring
- maintenance

You only need to upload the code and define the trigger.

---

# 2. What is Serverless Computing?

Serverless computing is a cloud computing model where **developers run code without managing infrastructure or servers**.

The cloud provider automatically manages:

- servers
- scaling
- availability

AWS Lambda is an example of serverless computing.

---

# 3. What languages are supported by AWS Lambda?

AWS Lambda supports multiple programming languages such as:

- Python
- Node.js
- Java
- Go
- Ruby
- .NET
- Custom runtime

---

# 4. What is a Lambda Function?

A Lambda function is **a piece of code that runs in response to events**.

Example triggers:

- S3 file upload
- API Gateway request
- DynamoDB update
- CloudWatch event

---

# 5. What are Lambda Triggers?

Triggers are **AWS services that invoke a Lambda function automatically**.

Examples:

- API Gateway
- S3
- DynamoDB
- CloudWatch
- SNS
- SQS

---

# 6. What is the maximum execution time for AWS Lambda?

The maximum execution time for a Lambda function is:

```
15 minutes
```

---

# 7. What is the memory limit for AWS Lambda?

Lambda memory can be configured between:

```
128 MB to 10 GB
```

Memory configuration also affects CPU performance.

---

# 8. What is AWS Lambda concurrency?

Concurrency refers to the **number of Lambda functions that can run simultaneously**.

AWS automatically scales Lambda based on incoming requests.

---

# 9. What is cold start in AWS Lambda?

Cold start occurs when **AWS initializes a new Lambda execution environment before running the function**.

This may slightly increase response time during the first request.

---

# 10. What is AWS Lambda timeout?

Timeout defines **how long Lambda waits before stopping execution**.

Maximum timeout:

```
900 seconds (15 minutes)
```

---

# 11. What is Lambda Layer?

Lambda layers allow you to **share libraries and dependencies across multiple Lambda functions**.

Example:

```
Common Python libraries
Shared utility code
```

---

# 12. What is Lambda Environment Variable?

Environment variables allow you to **store configuration settings outside the code**.

Example:

```
DATABASE_URL
API_KEY
```

---

# 13. What is AWS Lambda pricing based on?

Lambda pricing depends on:

- number of requests
- execution duration
- memory allocation

You only pay for **actual compute time used**.

---

# 14. What is the relationship between Lambda and API Gateway?

API Gateway can trigger Lambda functions to **create serverless APIs**.

Architecture example:

```
Client → API Gateway → Lambda → Database
```

---

# 15. What are some common use cases of AWS Lambda?

Common use cases include:

- serverless APIs
- real-time file processing
- data transformation
- automation scripts
- event-driven applications

---

# 16. What is AWS Lambda monitoring?

Lambda monitoring can be done using:

- AWS CloudWatch Logs
- CloudWatch Metrics
- AWS X-Ray

These tools help track:

- execution logs
- errors
- performance

---

# 17. What is the deployment package in Lambda?

A deployment package is a **ZIP file containing Lambda code and dependencies**.

Example:

```
function code
libraries
configuration files
```

---

# 18. What is the Lambda execution role?

Each Lambda function runs with an **IAM execution role**.

This role defines which AWS services the Lambda function can access.

Example permissions:

```
S3 access
DynamoDB access
CloudWatch logs
```

---

# 19. What is event-driven architecture in Lambda?

Event-driven architecture means **Lambda functions run when an event occurs**.

Example events:

```
File uploaded to S3
Message in SQS
HTTP request via API Gateway
```

---

# 20. Why is AWS Lambda important for DevOps?

Lambda helps DevOps teams:

- automate workflows
- build serverless applications
- reduce infrastructure management
- scale automatically
- reduce operational costs
