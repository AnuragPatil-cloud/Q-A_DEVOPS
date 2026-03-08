# ☸ Amazon EKS Scenario-Based DevOps Interview Questions

This section contains **real-world troubleshooting scenarios related to Amazon EKS (Elastic Kubernetes Service)** that DevOps engineers commonly face.

---

# Scenario 1: Pods Stuck in Pending State

### Problem
Pods are not starting and remain in **Pending** state.

### Possible Causes

- Insufficient resources in worker nodes
- No available nodes
- Incorrect node selector
- Taints and tolerations mismatch

### Solution

Check node availability:

```
kubectl get nodes
```

Check pod details:

```
kubectl describe pod <pod-name>
```

Verify resource requests and node configuration.

---

# Scenario 2: Pods in CrashLoopBackOff

### Problem
Pods repeatedly crash and restart.

### Possible Causes

- Application error
- Wrong environment variables
- Incorrect configuration
- Missing dependencies

### Solution

Check logs:

```
kubectl logs <pod-name>
```

Describe pod:

```
kubectl describe pod <pod-name>
```

Fix application or configuration issues.

---

# Scenario 3: Node Not Joining EKS Cluster

### Problem
EC2 worker nodes are not joining the cluster.

### Possible Causes

- Incorrect IAM role
- Wrong security group configuration
- Missing bootstrap script
- VPC networking issue

### Solution

Verify IAM role attached to worker nodes.

Check node logs:

```
/var/log/messages
```

Verify security groups and VPC settings.

---

# Scenario 4: Load Balancer Not Routing Traffic

### Problem
Application deployed on EKS is not accessible through the load balancer.

### Possible Causes

- Service type incorrect
- Target group not configured
- Security group blocking traffic

### Solution

Check service configuration:

```
kubectl get svc
```

Ensure service type is:

```
LoadBalancer
```

Verify target group health and security group rules.

---

# Scenario 5: EKS Pods Cannot Access AWS Services

### Problem
Pods cannot access AWS services such as S3 or DynamoDB.

### Cause

IAM permissions missing.

### Solution

Use **IAM Role for Service Account (IRSA)**.

Steps:

1. Create IAM role
2. Attach required policies
3. Associate role with Kubernetes service account

---

# Scenario 6: High CPU Usage in Pods

### Problem
Pods are consuming high CPU and performance is degraded.

### Solution

Enable **Horizontal Pod Autoscaler (HPA)**.

Example command:

```
kubectl autoscale deployment myapp --cpu-percent=70 --min=2 --max=10
```

This automatically scales pods based on CPU usage.

---

# Scenario 7: EKS Cluster Not Scaling Nodes

### Problem
Pods are pending because nodes are not scaling.

### Cause

Cluster Autoscaler not configured.

### Solution

Deploy Cluster Autoscaler.

It automatically adjusts the number of worker nodes based on workload.

---

# Scenario 8: Application Cannot Access Database

### Problem
Application pods cannot connect to database.

### Possible Causes

- Security group blocking traffic
- Wrong service endpoint
- DNS issue

### Solution

Check service:

```
kubectl get svc
```

Test DNS resolution inside pod:

```
kubectl exec -it <pod> -- nslookup database-service
```

---

# Scenario 9: Container Image Pull Error

### Problem
Pod shows error:

```
ImagePullBackOff
```

### Possible Causes

- Incorrect image name
- Private registry authentication issue
- Image not available

### Solution

Verify image name in deployment file.

Check events:

```
kubectl describe pod <pod-name>
```

Ensure registry credentials are configured.

---

# Scenario 10: Kubernetes Deployment Not Updating

### Problem
New application version not deployed.

### Cause

Rolling update not triggered.

### Solution

Restart deployment:

```
kubectl rollout restart deployment <deployment-name>
```

Check rollout status:

```
kubectl rollout status deployment <deployment-name>
```

---

# Scenario 11: EKS Cluster Networking Issue

### Problem
Pods cannot communicate with each other.

### Cause

CNI plugin misconfiguration.

### Solution

Check AWS VPC CNI plugin:

```
kubectl get pods -n kube-system
```

Restart networking components if required.

---

# Scenario 12: Need Zero Downtime Deployment

### Problem
Application downtime during updates.

### Solution

Use **Rolling Updates** in Kubernetes.

Example deployment strategy:

```
strategy:
  type: RollingUpdate
```

This updates pods gradually without downtime.

---

# 🎯 Why EKS Scenarios Are Important for DevOps

DevOps engineers working with EKS must troubleshoot:

- pod failures
- networking issues
- IAM permission problems
- scaling challenges
- deployment errors

Understanding these scenarios helps maintain **highly available and scalable Kubernetes applications**.
