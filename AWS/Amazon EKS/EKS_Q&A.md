# ☸ Amazon EKS Interview Questions & Answers

This section contains commonly asked **Amazon EKS (Elastic Kubernetes Service) interview questions** for DevOps engineers.

---

# 1. What is Amazon EKS?

Amazon EKS (Elastic Kubernetes Service) is a **managed Kubernetes service provided by AWS** that allows you to run Kubernetes clusters without managing the control plane.

AWS manages:

- Kubernetes control plane
- etcd
- high availability
- scaling

---

# 2. What is Kubernetes?

Kubernetes is an **open-source container orchestration platform** used to automate the deployment, scaling, and management of containerized applications.

---

# 3. Why do we use Amazon EKS?

Amazon EKS helps organizations:

- run Kubernetes without managing infrastructure
- scale applications automatically
- integrate Kubernetes with AWS services
- improve reliability and availability

---

# 4. What components does AWS manage in EKS?

AWS manages the **Kubernetes control plane**, which includes:

- API server
- etcd
- scheduler
- controller manager

This ensures high availability and reliability.

---

# 5. What components do users manage in EKS?

Users manage:

- worker nodes
- Kubernetes workloads
- deployments
- services
- networking configuration

---

# 6. What are EKS worker nodes?

Worker nodes are **EC2 instances that run containerized applications inside Kubernetes pods**.

They communicate with the Kubernetes control plane.

---

# 7. What is a node group in EKS?

A node group is a **set of worker nodes in an EKS cluster**.

Two types:

- Managed Node Groups
- Self-managed Node Groups

---

# 8. What is a managed node group?

Managed node groups are **automatically managed by AWS**.

AWS handles:

- provisioning
- scaling
- updating nodes

---

# 9. What is Fargate in EKS?

AWS Fargate allows running Kubernetes pods **without managing EC2 worker nodes**.

Benefits:

- serverless Kubernetes
- automatic scaling
- no server management

---

# 10. What is the role of kubectl in EKS?

`kubectl` is the **command-line tool used to interact with Kubernetes clusters**.

Example commands:

```
kubectl get pods
kubectl get nodes
kubectl apply -f deployment.yaml
```

---

# 11. What networking is used in Amazon EKS?

Amazon EKS uses the **AWS VPC networking model**.

Each pod receives an IP address from the VPC.

Networking is handled using the **AWS VPC CNI plugin**.

---

# 12. What is the AWS VPC CNI plugin?

The AWS VPC CNI plugin allows Kubernetes pods to **receive IP addresses directly from the VPC**.

This enables seamless networking between:

- pods
- services
- AWS resources

---

# 13. What is IAM role for service account (IRSA)?

IRSA allows Kubernetes pods to **securely access AWS services using IAM roles**.

Example:

```
Pod → IAM Role → S3 Access
```

This avoids storing AWS credentials inside pods.

---

# 14. What is an EKS cluster?

An EKS cluster consists of:

- Kubernetes control plane
- worker nodes
- networking configuration

Applications are deployed as **pods within the cluster**.

---

# 15. What are common tools used with EKS?

Common tools used with EKS include:

- kubectl
- Helm
- ArgoCD
- Terraform
- AWS CLI
- Docker

---

# 16. What monitoring tools are used for EKS?

Monitoring tools include:

- Amazon CloudWatch
- Prometheus
- Grafana

These tools help monitor:

- cluster health
- pod performance
- resource usage

---

# 17. What is EKS autoscaling?

EKS supports autoscaling using:

- Kubernetes Horizontal Pod Autoscaler (HPA)
- Cluster Autoscaler
- Auto Scaling Groups

This allows automatic scaling of pods and nodes.

---

# 18. What security features does EKS provide?

EKS provides multiple security features:

- IAM authentication
- VPC isolation
- security groups
- Kubernetes RBAC

These help secure Kubernetes workloads.

---

# 19. What are common use cases of Amazon EKS?

Common use cases include:

- microservices applications
- containerized workloads
- CI/CD pipelines
- scalable web applications
- machine learning workloads

---

# 20. Why is EKS important for DevOps?

EKS helps DevOps teams:

- run Kubernetes clusters easily
- automate deployments
- scale applications efficiently
- integrate Kubernetes with AWS services
