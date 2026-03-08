# 🚀 ArgoCD Interview Questions & Answers (DevOps)

This section contains commonly asked **ArgoCD interview questions for DevOps Engineers (Fresher – 2+ Years Experience).**

---

# 1. What is ArgoCD?

ArgoCD is an **open-source GitOps continuous delivery tool for Kubernetes**.

It automatically deploys applications to Kubernetes clusters by syncing the cluster state with configuration stored in a Git repository.

---

# 2. What is GitOps?

GitOps is a **deployment methodology where Git is used as the single source of truth for infrastructure and application configuration**.

Workflow:

```
Developer → Git Repository → ArgoCD → Kubernetes Cluster
```

---

# 3. Why do we use ArgoCD?

ArgoCD helps with:

- Automated Kubernetes deployments
- GitOps-based workflows
- Continuous delivery
- Easy rollbacks
- Monitoring application state

---

# 4. What are the main components of ArgoCD?

Main components:

- API Server
- Repository Server
- Application Controller
- ArgoCD UI

---

# 5. What is an ArgoCD Application?

An ArgoCD Application is a **custom resource that defines how an application is deployed in Kubernetes**.

It specifies:

- Git repository
- Kubernetes cluster
- Deployment configuration

---

# 6. What is the ArgoCD Application Controller?

The Application Controller continuously **monitors the desired state in Git and the live state in Kubernetes**.

If there is a difference, ArgoCD can automatically sync them.

---

# 7. What is Sync in ArgoCD?

Sync means **applying the configuration from Git to the Kubernetes cluster**.

Types:

- Manual Sync
- Automatic Sync

---

# 8. What is Auto Sync in ArgoCD?

Auto Sync automatically **updates the Kubernetes cluster when changes are pushed to Git**.

Benefits:

- Fully automated deployment
- Faster updates
- Reduced manual work

---

# 9. What is Drift Detection?

Drift detection identifies when the **live Kubernetes cluster state differs from the desired state defined in Git**.

ArgoCD highlights these differences.

---

# 10. What is Rollback in ArgoCD?

Rollback allows **reverting to a previous application version stored in Git**.

This helps recover quickly from faulty deployments.

---

# 11. What is the ArgoCD UI?

ArgoCD provides a **web-based dashboard** to manage applications and view deployment status.

Example access:

```
http://argocd-server
```

---

# 12. What is the ArgoCD CLI?

ArgoCD provides a command-line interface for managing applications.

Example commands:

```
argocd login
argocd app list
argocd app sync
argocd app delete
```

---

# 13. How do you install ArgoCD?

Example using Kubernetes:

```
kubectl create namespace argocd

kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
```

---

# 14. What is the default ArgoCD namespace?

ArgoCD is typically installed in:

```
argocd
```

---

# 15. Real DevOps Scenario

### Problem

Application deployment is inconsistent across environments.

### Solution

Use ArgoCD with GitOps workflow:

1. Store Kubernetes manifests in Git
2. ArgoCD monitors Git repository
3. Automatically sync changes to Kubernetes cluster

This ensures **consistent deployments across environments.**

---

# 16. Benefits of ArgoCD

- GitOps-based deployment
- Automated Kubernetes delivery
- Easy rollback
- Real-time application monitoring
- Secure and auditable deployments

---

# 🚀 Why ArgoCD is Important for DevOps

ArgoCD helps DevOps teams:

- Automate Kubernetes deployments
- Maintain consistent infrastructure
- Track deployment history
- Improve reliability of deployments

Common integrations:

- Kubernetes
- Helm
- GitHub
- GitLab
- Jenkins
- Terraform
