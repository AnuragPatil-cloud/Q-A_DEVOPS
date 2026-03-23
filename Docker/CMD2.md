# 🐳 Docker Commands with Real DevOps Usage (2+ Years Experience)

This section contains:

- Docker commands  
- Explanation  
- Real DevOps usage in production  

---

# 📌 1. docker build

```
docker build -t myapp .
```

## Explanation
Builds a Docker image from a Dockerfile.

## DevOps Usage
👉 Used in CI/CD pipelines to create application images before deployment.

Example:
- Jenkins builds image after code push
- GitHub Actions builds image

---

# 📌 2. docker run

```
docker run -d -p 80:80 nginx
```

## Explanation
Runs a container from an image.

## DevOps Usage
👉 Used to deploy applications quickly in testing or production.

Example:
- Run app container in staging server
- Test container before pushing to Kubernetes

---

# 📌 3. docker ps

```
docker ps
```

## Explanation
Shows running containers.

## DevOps Usage
👉 Used to check if application container is running in production.

---

# 📌 4. docker logs

```
docker logs <container-id>
```

## Explanation
Shows logs of container.

## DevOps Usage
👉 Used to debug issues like:
- app crash
- API failure
- database connection error

---

# 📌 5. docker exec

```
docker exec -it <container-id> /bin/bash
```

## Explanation
Access container terminal.

## DevOps Usage
👉 Used for:
- debugging inside container
- checking configs
- running manual commands

---

# 📌 6. docker stop / start

```
docker stop <id>
docker start <id>
```

## Explanation
Stops or starts container.

## DevOps Usage
👉 Used during:
- deployment restart
- troubleshooting

---

# 📌 7. docker rm / rmi

```
docker rm <id>
docker rmi <image-id>
```

## Explanation
Removes container/image.

## DevOps Usage
👉 Used to:
- clean unused containers
- save disk space

---

# 📌 8. docker pull

```
docker pull nginx
```

## Explanation
Downloads image from registry.

## DevOps Usage
👉 Used in:
- server setup
- pipeline deployment

---

# 📌 9. docker push

```
docker push myrepo/myapp
```

## Explanation
Uploads image to registry.

## DevOps Usage
👉 Used in CI/CD:
- build → push → deploy

---

# 📌 10. docker network

```
docker network create mynetwork
```

## Explanation
Creates network for containers.

## DevOps Usage
👉 Used for:
- microservices communication
- backend + frontend connection

---

# 📌 11. docker volume

```
docker run -v myvolume:/data nginx
```

## Explanation
Stores persistent data.

## DevOps Usage
👉 Used for:
- database storage
- logs persistence

---

# 📌 12. docker-compose

```
docker-compose up -d
```

## Explanation
Runs multi-container apps.

## DevOps Usage
👉 Used for:
- full-stack apps (frontend + backend + DB)
- local testing before Kubernetes

---

# 📌 13. docker stats

```
docker stats
```

## Explanation
Shows resource usage.

## DevOps Usage
👉 Used for:
- monitoring CPU/memory
- detecting performance issues

---

# 📌 14. docker inspect

```
docker inspect <id>
```

## Explanation
Detailed container info.

## DevOps Usage
👉 Used to:
- get container IP
- check mounts and configs

---

# 📌 15. docker system prune

```
docker system prune -a
```

## Explanation
Removes unused resources.

## DevOps Usage
👉 Used to:
- free disk space in servers
- clean CI/CD runners

---

# 🚀 Real DevOps Workflow Example

## CI/CD Flow

1. Developer pushes code  
2. Pipeline runs:

```
docker build -t app .
docker push repo/app
```

3. Deployment:

```
docker run -d -p 80:80 app
```

---

# 🎯 Why This Matters in Interview

When interviewer asks:

👉 “How do you use Docker in your project?”

You answer:

- Build images using Dockerfile  
- Push to registry (ECR/DockerHub)  
- Deploy containers  
- Debug using logs & exec  
- Use volumes for persistence  
- Use docker-compose for multi-service apps  

---

# 💡 Pro Tip

👉 Always explain **real usage**, not just commands  

This is what makes you a **2+ years experienced DevOps engineer**
