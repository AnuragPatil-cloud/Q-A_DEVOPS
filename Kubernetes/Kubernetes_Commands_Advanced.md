# ☸ Kubernetes Commands with Real DevOps Usage (2+ Years Experience)

This section includes:

- Kubernetes commands  
- Explanation  
- Real DevOps usage in production  

---

# 📌 1. kubectl get

```
kubectl get pods
kubectl get svc
kubectl get nodes
```

## Explanation
Used to list Kubernetes resources.

## DevOps Usage
👉 First command used during troubleshooting to check cluster status.

Example:
- Check if pods are running
- Verify services

---

# 📌 2. kubectl describe

```
kubectl describe pod <pod-name>
```

## Explanation
Shows detailed information about a resource.

## DevOps Usage
👉 Used to debug issues like:
- Pod Pending
- Scheduling failure
- Events and errors

---

# 📌 3. kubectl logs

```
kubectl logs <pod-name>
```

## Explanation
Fetch logs from container.

## DevOps Usage
👉 Used for:
- debugging application errors
- checking crash logs

---

# 📌 4. kubectl exec

```
kubectl exec -it <pod-name> -- /bin/bash
```

## Explanation
Access container shell.

## DevOps Usage
👉 Used to:
- debug inside container
- verify config files
- test connectivity

---

# 📌 5. kubectl apply

```
kubectl apply -f deployment.yaml
```

## Explanation
Creates or updates resources.

## DevOps Usage
👉 Used in:
- CI/CD pipelines
- deployments using YAML

---

# 📌 6. kubectl delete

```
kubectl delete pod <pod-name>
kubectl delete -f deployment.yaml
```

## Explanation
Deletes resources.

## DevOps Usage
👉 Used to:
- remove faulty pods
- clean old deployments

---

# 📌 7. kubectl rollout

```
kubectl rollout status deployment myapp
kubectl rollout restart deployment myapp
```

## Explanation
Manages deployment updates.

## DevOps Usage
👉 Used for:
- checking deployment progress
- restarting app without downtime

---

# 📌 8. kubectl scale

```
kubectl scale deployment myapp --replicas=5
```

## Explanation
Changes number of pods.

## DevOps Usage
👉 Used during:
- traffic spike
- manual scaling

---

# 📌 9. kubectl expose

```
kubectl expose deployment myapp --type=NodePort --port=80
```

## Explanation
Exposes deployment as service.

## DevOps Usage
👉 Used to:
- make app accessible
- create services

---

# 📌 10. kubectl get events

```
kubectl get events
```

## Explanation
Shows cluster events.

## DevOps Usage
👉 Used to debug:
- scheduling issues
- pod failures

---

# 📌 11. kubectl top

```
kubectl top pod
kubectl top node
```

## Explanation
Shows resource usage.

## DevOps Usage
👉 Used for:
- monitoring CPU/memory
- performance troubleshooting

---

# 📌 12. kubectl config

```
kubectl config get-contexts
kubectl config use-context <context>
```

## Explanation
Manages cluster contexts.

## DevOps Usage
👉 Used when working with:
- multiple clusters (dev, staging, prod)

---

# 📌 13. kubectl port-forward

```
kubectl port-forward pod/<pod-name> 8080:80
```

## Explanation
Forward local port to pod.

## DevOps Usage
👉 Used for:
- debugging apps locally
- testing APIs

---

# 📌 14. kubectl cp

```
kubectl cp file.txt pod:/tmp/
```

## Explanation
Copy files between local and pod.

## DevOps Usage
👉 Used for:
- debugging
- transferring configs/logs

---

# 📌 15. kubectl edit

```
kubectl edit deployment myapp
```

## Explanation
Edit resource live.

## DevOps Usage
👉 Used for quick fixes in production (temporary)

---

# 📌 16. kubectl drain / cordon

```
kubectl cordon <node>
kubectl drain <node>
```

## Explanation
Marks node unschedulable.

## DevOps Usage
👉 Used during:
- node maintenance
- upgrades

---

# 📌 17. kubectl label

```
kubectl label pod mypod env=prod
```

## Explanation
Adds labels to resources.

## DevOps Usage
👉 Used for:
- grouping resources
- routing traffic

---

# 📌 18. kubectl annotate

```
kubectl annotate pod mypod team=devops
```

## Explanation
Adds metadata.

## DevOps Usage
👉 Used for:
- tracking ownership
- documentation

---

# 📌 19. kubectl get all

```
kubectl get all
```

## Explanation
Shows all resources in namespace.

## DevOps Usage
👉 Quick overview during troubleshooting.

---

# 📌 20. kubectl apply -k (Kustomize)

```
kubectl apply -k .
```

## Explanation
Deploy using Kustomize.

## DevOps Usage
👉 Used for:
- environment-based deployments
- GitOps workflows

---

# 🚀 Real DevOps Workflow Example

## Deployment Flow

1. Developer pushes code  
2. CI builds Docker image  
3. CD deploys:

```
kubectl apply -f deployment.yaml
```

4. Monitor:

```
kubectl get pods
kubectl logs <pod>
```

---

# 🎯 Interview Answer Tip

If asked:

👉 “How do you use Kubernetes in your project?”

Say:

- Deploy apps using YAML files  
- Manage pods, services, deployments  
- Debug using logs and describe  
- Scale using kubectl scale  
- Monitor using kubectl top  
- Perform rolling updates  

---

# 💡 Pro Tip

👉 Always explain **real production usage + troubleshooting**

This shows you are a **real DevOps engineer, not just theoretical**
