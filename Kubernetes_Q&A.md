# ☸ Kubernetes Interview Questions & Answers (DevOps)

This section contains commonly asked **Kubernetes interview questions for DevOps Engineers (Fresher – 2+ Years Experience).**

---

# 1. What is Kubernetes?

Kubernetes is an **open-source container orchestration platform** used to automate the deployment, scaling, and management of containerized applications.

It was originally developed by Google.

---

# 2. Why do we use Kubernetes?

Kubernetes helps in:

- Automating container deployment
- Scaling applications
- Managing container networking
- Load balancing
- Self-healing of containers
- Rolling updates

---

# 3. What is a Kubernetes Cluster?

A Kubernetes cluster is a **set of nodes that run containerized applications**.

A cluster consists of:

Master Node (Control Plane)  
Worker Nodes

---

# 4. Kubernetes Architecture

Control Plane Components:

- API Server
- Scheduler
- Controller Manager
- etcd

Worker Node Components:

- Kubelet
- Kube Proxy
- Container Runtime (Docker / containerd)

---

# 5. What is a Pod?

A Pod is the **smallest deployable unit in Kubernetes**.

It contains:

- One or more containers
- Shared storage
- Network

Example Pod YAML:

```yaml
apiVersion: v1
kind: Pod
metadata:
  name: nginx-pod
spec:
  containers:
  - name: nginx
    image: nginx
```

---

# 6. What is a Deployment?

A Deployment is used to **manage multiple replicas of Pods** and provide updates and rollbacks.

Example:

```yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: nginx-deployment
spec:
  replicas: 3
  selector:
    matchLabels:
      app: nginx
  template:
    metadata:
      labels:
        app: nginx
    spec:
      containers:
      - name: nginx
        image: nginx
```

---

# 7. What is a Service in Kubernetes?

A Service exposes a set of Pods and provides **stable networking**.

Types of services:

- ClusterIP
- NodePort
- LoadBalancer
- ExternalName

---

# 8. What is NodePort Service?

NodePort exposes the application on a **port of the worker node**.

Example:

```yaml
apiVersion: v1
kind: Service
metadata:
  name: nginx-service
spec:
  type: NodePort
  selector:
    app: nginx
  ports:
  - port: 80
    targetPort: 80
    nodePort: 30007
```

---

# 9. What is a ReplicaSet?

ReplicaSet ensures that a **specified number of pod replicas are always running**.

Example:

```
replicas: 3
```

This ensures 3 pods are always available.

---

# 10. What is ConfigMap?

ConfigMap is used to store **configuration data in key-value pairs**.

Example:

```yaml
apiVersion: v1
kind: ConfigMap
metadata:
  name: app-config
data:
  app_name: devops-app
```

---

# 11. What is a Secret?

Secrets store **sensitive data such as passwords, tokens, or keys**.

Examples:

- Database password
- API keys
- Certificates

---

# 12. What is Ingress?

Ingress manages **external access to services inside the cluster**, usually HTTP/HTTPS.

It acts as a **Layer 7 load balancer**.

---

# 13. Important kubectl Commands

```
kubectl get pods
kubectl get nodes
kubectl describe pod pod-name
kubectl logs pod-name
kubectl apply -f file.yaml
kubectl delete pod pod-name
kubectl exec -it pod-name -- /bin/bash
```

---

# 14. How do you check cluster nodes?

```
kubectl get nodes
```

---

# 15. How do you check running pods?

```
kubectl get pods
```

---

# 16. How do you check pod details?

```
kubectl describe pod pod-name
```

---

# 17. How do you check pod logs?

```
kubectl logs pod-name
```

---

# 18. What is CrashLoopBackOff?

CrashLoopBackOff means a container **keeps crashing and Kubernetes is restarting it repeatedly**.

Possible causes:

- Application error
- Wrong configuration
- Missing environment variables
- Port conflict

Check logs:

```
kubectl logs pod-name
```

---

# 19. What is Horizontal Pod Autoscaler (HPA)?

HPA automatically **scales pods based on CPU or memory usage**.

Example:

```
kubectl autoscale deployment nginx --cpu-percent=50 --min=1 --max=10
```

---

# 20. What is Rolling Update?

Rolling update allows updating applications **without downtime** by gradually replacing old pods with new ones.

---

# 21. What is Namespace?

Namespaces are used to **logically separate resources within a cluster**.

Example namespaces:

- default
- kube-system
- dev
- prod

---

# 22. What is etcd?

etcd is a **distributed key-value store** used by Kubernetes to store cluster data.

---

# 23. What is Kubelet?

Kubelet is an **agent running on each worker node** that communicates with the API server and manages containers.

---

# 24. What is Kube Proxy?

Kube Proxy manages **network communication between services and pods**.

---

# 25. Real DevOps Kubernetes Troubleshooting

### Problem: Pod not starting

Check pod details:

```
kubectl describe pod pod-name
```

Check logs:

```
kubectl logs pod-name
```

---

### Problem: Pod stuck in Pending state

Possible reasons:

- No available node resources
- Node not ready
- Scheduling issues

Check nodes:

```
kubectl get nodes
```

---

### Problem: ImagePullBackOff error

Possible causes:

- Wrong image name
- Image not available in registry
- Authentication issue

---

# 🚀 Why Kubernetes is Important for DevOps

Kubernetes is used for:

- Container orchestration
- Auto scaling applications
- High availability
- Rolling updates
- Microservices architecture

Kubernetes integrates with:

- Docker
- Helm
- Prometheus
- Grafana
- AWS EKS
- Terraform
