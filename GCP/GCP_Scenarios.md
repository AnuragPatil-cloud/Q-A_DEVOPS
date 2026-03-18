# ☁ Google Cloud Platform (GCP) Scenario-Based DevOps Interview Questions

This section contains **real-world GCP troubleshooting scenarios** commonly faced by DevOps engineers.

---

# Scenario 1: GCP VM Not Accessible via SSH

### Problem
Unable to connect to a Compute Engine VM using SSH.

### Possible Causes

- firewall rules blocking SSH (port 22)
- VM not running
- incorrect external IP
- OS login issues

### Solution

Check firewall rules:

```
Allow tcp:22
```

Verify VM status and external IP.

---

# Scenario 2: Application Not Accessible via Load Balancer

### Problem
Users cannot access the application through GCP Load Balancer.

### Possible Causes

- backend instance not healthy
- firewall blocking traffic
- incorrect backend service configuration

### Solution

Check backend health:

```
GCP Console → Load Balancer → Backend Services
```

Verify firewall rules for HTTP/HTTPS.

---

# Scenario 3: GKE Pod Not Starting

### Problem
Pod remains in **Pending** or **CrashLoopBackOff** state.

### Possible Causes

- insufficient resources
- incorrect image
- configuration errors

### Solution

Check pod:

```
kubectl describe pod <pod-name>
kubectl logs <pod-name>
```

Fix image or resource configuration.

---

# Scenario 4: Cannot Pull Image in GKE

### Problem
Pod shows error:

```
ImagePullBackOff
```

### Possible Causes

- wrong image name
- private registry authentication issue

### Solution

Verify image name and credentials.

Ensure GKE has access to container registry.

---

# Scenario 5: Cloud Storage Access Denied

### Problem
Application cannot access Cloud Storage bucket.

### Cause

IAM permissions missing.

### Solution

Assign role:

```
Storage Object Viewer
Storage Object Admin
```

Check bucket permissions.

---

# Scenario 6: High CPU Usage in VM

### Problem
Application performance is slow due to high CPU usage.

### Solution

Use:

```
Cloud Monitoring
```

Identify process and optimize or scale VM.

---

# Scenario 7: Cloud Function Not Triggering

### Problem
Cloud Function does not execute after event.

### Possible Causes

- incorrect trigger configuration
- permission issues

### Solution

Verify trigger source:

```
HTTP / PubSub / Storage
```

Check logs in Cloud Logging.

---

# Scenario 8: Logs Not Appearing in Cloud Logging

### Problem
Application logs are missing.

### Cause

Logging not configured or insufficient permissions.

### Solution

Enable logging and verify IAM roles.

Check logs in:

```
Cloud Logging → Logs Explorer
```

---

# Scenario 9: Autoscaling Not Working in GCP

### Problem
Application load increases but instances are not scaling.

### Cause

Incorrect autoscaling configuration.

### Solution

Check autoscaling policy:

```
CPU utilization threshold
Min/Max instances
```

Ensure monitoring metrics are enabled.

---

# Scenario 10: Need High Availability Architecture

### Problem
Application must be highly available.

### Solution

Use:

- multiple zones
- load balancer
- autoscaling

Architecture:

```
Users
   ↓
Load Balancer
   ↓
Multiple VMs (different zones)
```

---

# 🎯 Why GCP Scenarios Are Important for DevOps

DevOps engineers must troubleshoot:

- VM connectivity issues
- container deployment failures
- IAM permission errors
- storage access problems
- scaling issues

Understanding these scenarios helps maintain **reliable and scalable cloud infrastructure in GCP**.
