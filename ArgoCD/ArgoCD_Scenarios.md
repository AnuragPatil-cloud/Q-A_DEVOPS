# 🚀 ArgoCD Scenario-Based DevOps Interview Questions

This section contains **real-world ArgoCD troubleshooting scenarios** commonly faced by DevOps engineers when working with Kubernetes GitOps deployments.

---

# Scenario 1: ArgoCD Application Showing OutOfSync

### Problem
ArgoCD application status shows:

```
OutOfSync
```

### Cause

The live state of the application in the Kubernetes cluster is different from the desired state stored in Git.

### Solution

Perform manual sync:

```
argocd app sync <application-name>
```

Or enable **auto-sync** in the application configuration.

---

# Scenario 2: ArgoCD Not Detecting Changes from Git

### Problem
Code changes pushed to Git repository but ArgoCD does not update the deployment.

### Possible Causes

- Auto sync disabled
- Incorrect repository configuration
- Webhook not configured

### Solution

Verify:

```
Repository configuration
Application sync settings
Git webhook configuration
```

Manually refresh application if required.

---

# Scenario 3: ArgoCD Cannot Access Git Repository

### Problem
ArgoCD fails to fetch code from Git.

### Possible Causes

- Invalid repository credentials
- SSH key not configured
- Git repository permissions issue

### Solution

Check repository access:

```
argocd repo list
```

Update repository credentials in ArgoCD.

---

# Scenario 4: Deployment Fails After Sync

### Problem
ArgoCD sync completes but application pods fail.

### Cause

Application configuration issue or container failure.

### Solution

Check Kubernetes resources:

```
kubectl get pods
kubectl describe pod <pod-name>
kubectl logs <pod-name>
```

Fix deployment configuration in Git.

---

# Scenario 5: ArgoCD Application Stuck in Progressing State

### Problem
Application status remains:

```
Progressing
```

### Possible Causes

- pods not ready
- deployment rollout incomplete
- failing readiness probes

### Solution

Check deployment status:

```
kubectl rollout status deployment <deployment-name>
```

Verify readiness and liveness probes.

---

# Scenario 6: ArgoCD Cannot Access Kubernetes Cluster

### Problem
ArgoCD fails to deploy resources to the cluster.

### Cause

Cluster credentials not configured correctly.

### Solution

Check cluster connection:

```
argocd cluster list
```

Re-register cluster if necessary.

---

# Scenario 7: ArgoCD Sync Deletes Existing Resources

### Problem
Some Kubernetes resources get deleted during sync.

### Cause

Resources not defined in Git repository.

ArgoCD follows **Git as the source of truth**.

### Solution

Ensure all required resources are defined in Git manifests.

---

# Scenario 8: Helm Chart Deployment Failing in ArgoCD

### Problem
Application using Helm chart fails to deploy.

### Possible Causes

- incorrect values.yaml
- incompatible Helm chart version

### Solution

Verify Helm configuration and values.

Test locally:

```
helm template .
```

Fix configuration and commit changes to Git.

---

# Scenario 9: ArgoCD Permission Error

### Problem
Users cannot access applications in ArgoCD UI.

### Cause

RBAC permissions not configured.

### Solution

Update RBAC configuration in:

```
argocd-rbac-cm
```

Assign correct roles to users.

---

# Scenario 10: Need Rollback After Failed Deployment

### Problem
New deployment caused application failure.

### Solution

Rollback to previous version:

```
argocd app rollback <app-name> <revision>
```

Or revert changes in Git.

---

# 🎯 Why ArgoCD Scenarios Are Important for DevOps

DevOps engineers using ArgoCD must troubleshoot:

- Git synchronization issues
- Kubernetes deployment failures
- permission errors
- repository access problems
- cluster connectivity issues

Understanding these scenarios helps maintain **reliable GitOps-based Kubernetes deployments**.
