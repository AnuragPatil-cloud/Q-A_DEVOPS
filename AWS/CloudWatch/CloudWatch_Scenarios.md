# 📊 AWS CloudWatch Scenario-Based DevOps Interview Questions

This section contains **real-world AWS CloudWatch troubleshooting scenarios** commonly faced by DevOps engineers.

---

# Scenario 1: CPU Alarm Not Triggering

### Problem
CPU utilization is above 80% but the CloudWatch alarm is not triggered.

### Possible Causes

- Alarm threshold incorrectly configured
- Wrong metric selected
- Evaluation period too high

### Solution

Check alarm configuration:

```
CloudWatch → Alarms → Alarm Settings
```

Verify:

- correct metric
- threshold value
- evaluation period

---

# Scenario 2: Logs Not Appearing in CloudWatch

### Problem
Application logs are not visible in CloudWatch Logs.

### Possible Causes

- CloudWatch agent not installed
- IAM role missing permissions
- Incorrect log group configuration

### Solution

Verify CloudWatch agent status:

```
systemctl status amazon-cloudwatch-agent
```

Ensure IAM role includes:

```
CloudWatchLogsFullAccess
```

---

# Scenario 3: EC2 Memory Metrics Not Available

### Problem
CloudWatch shows CPU metrics but not memory usage.

### Cause

CloudWatch does not collect memory metrics by default.

### Solution

Install and configure **CloudWatch Agent** on EC2.

Steps:

```
Install CloudWatch Agent
Configure memory metrics
Start agent service
```

---

# Scenario 4: Auto Scaling Not Triggering

### Problem
Auto Scaling should launch new instances when CPU usage is high but it does not.

### Possible Causes

- Alarm not connected to scaling policy
- Incorrect scaling configuration

### Solution

Check:

```
Auto Scaling Group → Scaling Policies
```

Ensure CloudWatch alarm is linked to the scaling policy.

---

# Scenario 5: Lambda Logs Missing

### Problem
Lambda function runs but logs are not visible in CloudWatch.

### Cause

Lambda execution role missing permissions.

### Solution

Attach policy:

```
AWSLambdaBasicExecutionRole
```

This allows Lambda to send logs to CloudWatch.

---

# Scenario 6: Too Many CloudWatch Alerts

### Problem
DevOps team receives too many alerts.

### Cause

Improper alarm configuration.

### Solution

Use:

- Composite alarms
- proper threshold tuning
- alarm aggregation

This reduces alert noise.

---

# Scenario 7: Application Error Monitoring

### Problem
Need to detect application errors automatically.

### Solution

Use **CloudWatch Metric Filters**.

Example:

Count log entries containing:

```
ERROR
```

Trigger an alarm if error count increases.

---

# Scenario 8: High Disk Usage on EC2

### Problem
Disk usage increases but no alert is triggered.

### Cause

Disk metrics not configured.

### Solution

Configure CloudWatch Agent to collect:

```
disk_used_percent
```

Then create alarm.

---

# Scenario 9: Need Centralized Logs from Multiple Servers

### Problem
Logs from multiple EC2 servers need centralized monitoring.

### Solution

Use **CloudWatch Logs**.

Install CloudWatch agent on each server and send logs to a common log group.

---

# Scenario 10: Investigating High Network Traffic

### Problem
Unexpected network traffic detected.

### Solution

Use CloudWatch metrics to monitor:

```
NetworkIn
NetworkOut
```

Combine with **VPC Flow Logs** for deeper analysis.

---

# 🎯 Why CloudWatch Scenarios Are Important for DevOps

DevOps engineers must troubleshoot:

- infrastructure issues
- application failures
- performance bottlenecks
- scaling events
- logging problems

CloudWatch provides **critical monitoring and alerting capabilities in AWS environments**.
