# ☁ Azure Scenario-Based DevOps Interview Questions

This section contains **real-world Azure troubleshooting scenarios** commonly faced by DevOps engineers.

---

# Scenario 1: Azure VM Not Accessible via SSH or RDP

### Problem
You cannot connect to an Azure Virtual Machine.

### Possible Causes

- Network Security Group (NSG) blocking traffic
- VM not running
- Incorrect public IP
- Firewall rules blocking access

### Solution

Check NSG rules:

```
Allow SSH (22)
Allow RDP (3389)
```

Verify VM status and public IP address.

---

# Scenario 2: Application Not Accessible Through Azure Load Balancer

### Problem
Users cannot access the application through the load balancer.

### Possible Causes

- Backend pool not configured
- Health probe failing
- Network security rules blocking traffic

### Solution

Verify:

- backend pool configuration
- health probe status
- load balancer rules

Ensure backend VMs are healthy.

---

# Scenario 3: Azure Pipeline Build Failing

### Problem
CI/CD pipeline fails during build stage.

### Possible Causes

- dependency errors
- incorrect pipeline configuration
- environment variable issues

### Solution

Check pipeline logs in:

```
Azure DevOps → Pipelines → Logs
```

Fix build errors and update pipeline configuration.

---

# Scenario 4: Azure Kubernetes Service (AKS) Pod Not Starting

### Problem
Pods remain in **Pending** or **CrashLoopBackOff** state.

### Possible Causes

- insufficient node resources
- incorrect container image
- configuration errors

### Solution

Check pod details:

```
kubectl describe pod <pod-name>
kubectl logs <pod-name>
```

Verify container image and resource requests.

---

# Scenario 5: Azure Storage Access Denied

### Problem
Application cannot access Azure Storage.

### Possible Causes

- incorrect access key
- role-based access control issue
- storage firewall restrictions

### Solution

Verify storage access keys and IAM roles.

Check storage account network settings.

---

# Scenario 6: Azure Autoscaling Not Triggering

### Problem
Application traffic increases but autoscaling does not occur.

### Possible Causes

- incorrect scaling rules
- monitoring metrics not configured

### Solution

Check autoscaling settings:

```
Azure Monitor → Autoscale Settings
```

Ensure correct metrics and thresholds.

---

# Scenario 7: High CPU Usage on Azure VM

### Problem
VM performance is slow due to high CPU usage.

### Solution

Monitor metrics using:

```
Azure Monitor
```

Identify heavy processes and optimize application or scale VM resources.

---

# Scenario 8: Azure AKS Cannot Pull Container Image

### Problem
Pods fail with error:

```
ImagePullBackOff
```

### Possible Causes

- private container registry authentication issue
- incorrect image name
- network restrictions

### Solution

Verify container registry credentials and image name.

Ensure AKS has access to the container registry.

---

# Scenario 9: Application Logs Missing

### Problem
Application logs are not visible.

### Solution

Enable logging using:

```
Azure Monitor
Azure Log Analytics
```

Configure log collection for the application.

---

# Scenario 10: Need High Availability for Azure Application

### Problem
Application must remain available even if one VM fails.

### Solution

Use:

- Azure Load Balancer
- multiple availability zones
- autoscaling

Architecture:

```
Users
   ↓
Load Balancer
   ↓
Multiple VMs
```

---

# 🎯 Why Azure Scenarios Are Important for DevOps

DevOps engineers working with Azure must troubleshoot:

- VM connectivity issues
- pipeline failures
- container deployment problems
- storage access errors
- scaling issues

Understanding these scenarios helps maintain **reliable and scalable cloud infrastructure**.
