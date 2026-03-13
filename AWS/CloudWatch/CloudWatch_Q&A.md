# 📊 AWS CloudWatch Interview Questions & Answers

This section contains commonly asked **AWS CloudWatch interview questions** for DevOps engineers.

---

# 1. What is Amazon CloudWatch?

Amazon CloudWatch is a **monitoring and observability service that collects and tracks metrics, logs, and events from AWS resources and applications**.

It helps monitor system performance and troubleshoot issues.

---

# 2. What can CloudWatch monitor?

CloudWatch can monitor:

- EC2 instances
- RDS databases
- Lambda functions
- Load balancers
- custom application metrics

---

# 3. What are CloudWatch Metrics?

Metrics are **numerical data points representing the performance of AWS resources over time**.

Examples:

- CPU utilization
- network traffic
- disk usage
- request count

---

# 4. What are CloudWatch Logs?

CloudWatch Logs allow you to **collect, monitor, and store logs from applications and AWS services**.

Examples:

- application logs
- Lambda logs
- EC2 system logs

---

# 5. What is a CloudWatch Alarm?

A CloudWatch alarm monitors a metric and **triggers an action when the metric crosses a defined threshold**.

Example:

```
CPU utilization > 80%
```

The alarm can trigger:

- SNS notification
- Auto Scaling action
- Lambda function

---

# 6. What is CloudWatch Dashboard?

CloudWatch Dashboard allows you to **create visual dashboards to monitor AWS resources and metrics in one place**.

It can display:

- graphs
- metrics
- alarms

---

# 7. What is CloudWatch Events?

CloudWatch Events (now called **EventBridge**) allows AWS services to **trigger actions based on events**.

Example:

```
EC2 instance state change
```

---

# 8. What is a CloudWatch Log Group?

A log group is a **collection of log streams that share the same retention and monitoring settings**.

Example:

```
/aws/lambda/my-function
```

---

# 9. What is a CloudWatch Log Stream?

A log stream is a **sequence of log events from a specific source within a log group**.

Example:

Logs from a specific EC2 instance or Lambda execution.

---

# 10. What is CloudWatch Agent?

CloudWatch Agent is software installed on EC2 instances to **collect system-level metrics and logs**.

It can collect:

- memory usage
- disk utilization
- system logs

---

# 11. What is the difference between Basic Monitoring and Detailed Monitoring?

| Monitoring Type | Data Frequency |
|---|---|
Basic Monitoring | 5 minutes |
Detailed Monitoring | 1 minute |

Detailed monitoring provides more granular metrics.

---

# 12. What is CloudWatch Logs Retention?

Retention defines **how long logs are stored in CloudWatch**.

Example:

```
7 days
30 days
90 days
```

After the retention period, logs are automatically deleted.

---

# 13. What is CloudWatch Composite Alarm?

Composite alarms allow **combining multiple alarms into a single alarm condition**.

This reduces unnecessary alerts.

---

# 14. What is CloudWatch Contributor Insights?

Contributor Insights helps analyze **log data to identify top contributors to traffic or errors**.

Example:

- top IP addresses
- top API calls

---

# 15. What is CloudWatch Synthetics?

CloudWatch Synthetics monitors applications by running **automated scripts that simulate user interactions**.

This helps detect application issues before users experience them.

---

# 16. What is CloudWatch Container Insights?

Container Insights monitors **containers and Kubernetes clusters such as EKS**.

It provides visibility into:

- CPU usage
- memory usage
- container performance

---

# 17. What is CloudWatch Metric Filter?

Metric filters allow you to **convert log data into CloudWatch metrics**.

Example:

Count the number of error logs.

---

# 18. What actions can CloudWatch alarms trigger?

CloudWatch alarms can trigger actions such as:

- sending SNS notifications
- triggering Auto Scaling
- invoking Lambda functions

---

# 19. What is CloudWatch used for in DevOps?

DevOps engineers use CloudWatch for:

- infrastructure monitoring
- log management
- alerting
- troubleshooting
- performance analysis

---

# 20. Why is CloudWatch important for AWS environments?

CloudWatch helps ensure:

- system health monitoring
- early detection of issues
- automated alerts
- better operational visibility
