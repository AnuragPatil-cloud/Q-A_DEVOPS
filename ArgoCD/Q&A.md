# 🚀 ArgoCD Interview Questions & Answers (DevOps)

This section contains commonly asked **ArgoCD interview questions** for DevOps engineers.

---

# 1. What is ArgoCD?

ArgoCD is an **open-source GitOps continuous delivery tool used to deploy applications to Kubernetes clusters**.

It automatically synchronizes application configurations from a Git repository to a Kubernetes cluster.

---

# 2. What is GitOps?

GitOps is a **deployment approach where Git is used as the single source of truth for infrastructure and application configurations**.

Workflow:

```
Developer → Git Repository → ArgoCD → Kubernetes Cluster
```

---

# 3. Why do we use ArgoCD?

ArgoCD helps with:

- automated Kubernetes deployments
- Git-based version control for infrastructure
- continuous delivery
- rollback capability
- application state monitoring

---

# 4. What are the main components of ArgoCD?

ArgoCD architecture includes:

- API Server
- Repository Server
- Application Controller
- Web UI
- Redis

---

# 5. What is an ArgoCD Application?

An ArgoCD Application is a **custom resource that defines how an application should be deployed in Kubernetes**.

It includes:

- Git repository location
- Kubernetes cluster
- deployment configuration

---

# 6. What is ArgoCD Sync?

Sync is the process where **ArgoCD compares the desired state from Git with the live state in the Kubernetes cluster and applies changes if needed**.

Types of sync:

- Manual sync
- Automatic sync

---

# 7. What is Auto Sync in ArgoCD?

Auto Sync automatically **applies changes to the Kubernetes cluster whenever updates are pushed to the Git repository**.

This ensures continuous deployment.

---

# 8. What is Drift Detection in ArgoCD?

Drift detection identifies when **the live state of the application in Kubernetes differs from the desired state defined in Git**.

ArgoCD alerts the user when drift occurs.

---

# 9. What is Rollback in ArgoCD?

Rollback allows reverting to **a previous version of the application stored in Git** if a deployment fails.

This helps restore stable application versions.

---

# 10. What is the ArgoCD UI?

ArgoCD provides a **web-based dashboard** where users can:

- monitor application deployments
- view sync status
- perform manual sync operations

---

# 11. What is ArgoCD CLI?

ArgoCD CLI is a command-line tool used to interact with ArgoCD.

Common commands:

```
argocd login
argocd app list
argocd app sync
argocd app delete
```

---

# 12. What is the default namespace for ArgoCD?

ArgoCD is usually installed in the namespace:

```
argocd
```

---

# 13. What configuration files does ArgoCD use?

ArgoCD typically uses:

- Kubernetes manifests
- Helm charts
- Kustomize configurations

These files are stored in Git repositories.

---

# 14. What is ArgoCD Application Controller?

The application controller continuously monitors:

- desired state (Git repository)
- live state (Kubernetes cluster)

If differences are detected, ArgoCD updates the cluster.

---

# 15. What is the difference between ArgoCD and Jenkins?

| Feature | ArgoCD | Jenkins |
|---|---|---|
Purpose | Continuous Delivery | Continuous Integration |
Deployment | GitOps-based | Pipeline-based |
Focus | Kubernetes deployments | Build automation |

---

# 16. What tools integrate with ArgoCD?

Common integrations include:

- Kubernetes
- Helm
- GitHub
- GitLab
- Terraform
- Prometheus

---

# 17. What is ArgoCD Health Status?

ArgoCD monitors the health of deployed applications.

Possible states include:

```
Healthy
Progressing
Degraded
Missing
```

---

# 18. What is an ArgoCD Project?

A project is used to **organize and manage multiple applications with specific permissions and configurations**.

It helps enforce access control and policies.

---

# 19. What security features does ArgoCD provide?

ArgoCD supports:

- RBAC (Role-Based Access Control)
- Git authentication
- TLS encryption
- Kubernetes authentication

---

# 20. Why is ArgoCD important for DevOps?

ArgoCD helps DevOps teams:

- automate Kubernetes deployments
- maintain version-controlled infrastructure
- improve deployment reliability
- implement GitOps workflows
