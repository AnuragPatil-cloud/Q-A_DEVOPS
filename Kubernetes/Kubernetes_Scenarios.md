# ☸ Kubernetes Scenario-Based DevOps Interview Questions (Basic + Advanced)

This section contains **real-world Kubernetes troubleshooting scenarios** with **in-depth explanations and solutions**.

---

# 🔰 BASIC SCENARIOS

---

# Scenario 1: Pod in CrashLoopBackOff

## Problem
Pod is restarting continuously.

## Explanation
The application inside the container is failing repeatedly, so Kubernetes keeps restarting it.

## Troubleshooting

```
kubectl logs <pod-name>
kubectl describe pod <pod-name>
```

## Root Causes

- Application crash
- Wrong environment variables
- Missing dependencies
- Incorrect configuration

## Fix

- Fix application issue
- Update environment variables
- Redeploy

---

# Scenario 2: Pod in Pending State

## Problem
Pod is not getting scheduled.

## Explanation
Kubernetes scheduler cannot find a suitable node.

## Troubleshooting

```
kubectl describe pod <pod-name>
```

## Root Causes

- Insufficient CPU/Memory
- Node not ready
- Taints not tolerated

## Fix

- Add nodes
- Adjust resource requests
- Fix node issues

---

# Scenario 3: Service Not Accessible

## Problem
Application not reachable.

## Explanation
Service or networking issue.

## Troubleshooting

```
kubectl get svc
kubectl describe svc <service-name>
```

## Root Causes

- Wrong service type
- Port mismatch
- Pod not running

## Fix

- Correct service configuration
- Verify ports

---

# Scenario 4: ImagePullBackOff

## Problem
Pod cannot pull image.

## Explanation
Kubernetes cannot access container image.

## Root Causes

- Wrong image name
- Private registry authentication issue

## Fix

- Correct image name
- Add imagePullSecrets

---

# Scenario 5: ConfigMap Not Applied

## Problem
Application not using updated config.

## Explanation
Pods don’t automatically reload ConfigMaps.

## Fix

```
kubectl rollout restart deployment <name>
```

---

# 🚀 ADVANCED PRODUCTION SCENARIOS

---

# Scenario 6: High CPU Usage in Pods

## Problem
Pods consuming high CPU.

## Troubleshooting

```
kubectl top pod
```

## Root Causes

- Traffic spike
- Inefficient code

## Fix

- Enable HPA
- Optimize application

---

# Scenario 7: Node Not Ready

## Problem
Node shows NotReady.

## Troubleshooting

```
kubectl get nodes
kubectl describe node <node-name>
```

## Root Causes

- Kubelet stopped
- Network issue

## Fix

- Restart kubelet
- Check node health

---

# Scenario 8: Deployment Not Updating

## Problem
New version not deployed.

## Troubleshooting

```
kubectl rollout status deployment <name>
```

## Root Causes

- Image not updated
- Wrong tag (latest issue)

## Fix

- Use proper version tags
- Redeploy

---

# Scenario 9: Pods Not Scaling Automatically

## Problem
HPA not working.

## Troubleshooting

```
kubectl get hpa
```

## Root Causes

- Metrics server not installed
- Wrong thresholds

## Fix

- Install metrics server
- Configure HPA correctly

---

# Scenario 10: Ingress Not Working

## Problem
Application not accessible via domain.

## Troubleshooting

```
kubectl get ingress
```

## Root Causes

- Ingress controller not installed
- DNS issue

## Fix

- Install NGINX ingress controller
- Update DNS

---

# Scenario 11: Pod Cannot Connect to Database

## Problem
App cannot connect to DB.

## Root Causes

- Wrong service name
- Network policy blocking

## Fix

- Verify service DNS
- Check connectivity

---

# Scenario 12: Storage Not Persisting

## Problem
Data lost after pod restart.

## Root Cause

- No persistent volume

## Fix

- Use PVC (Persistent Volume Claim)

---

# Scenario 13: Too Many Restarts in Production

## Problem
Pods restarting frequently.

## Root Causes

- Liveness probe failing
- Resource limits exceeded

## Fix

- Adjust probes
- Increase resources

---

# Scenario 14: Rolling Update Causing Downtime

## Problem
Users experience downtime during deployment.

## Root Cause

- Improper deployment strategy

## Fix

Use:

```
strategy:
  rollingUpdate:
    maxUnavailable: 0
```

---

# Scenario 15: Cluster Performance Slow

## Problem
Applications slow.

## Troubleshooting

```
kubectl top node
```

## Root Causes

- Resource exhaustion
- Too many pods

## Fix

- Scale cluster
- Optimize workloads

---

# 🎯 FINAL INTERVIEW TIP

If interviewer asks:

👉 “How do you troubleshoot Kubernetes issues?”

Answer like this:

1. Check pod status  
```
kubectl get pods
```

2. Check logs  
```
kubectl logs <pod>
```

3. Describe resource  
```
kubectl describe pod <pod>
```

4. Check events  
```
kubectl get events
```

5. Verify resources (CPU/memory)  

---

# 🚀 Why This Section is Important

This proves:

✅ Real production experience  
✅ Troubleshooting skills  
✅ Kubernetes depth  
✅ DevOps maturity  
