# 🐳 Docker Commands for DevOps (2+ Years Experience)

This section contains **advanced and commonly used Docker commands** used by DevOps engineers in real-world projects.

---

# 📌 1. Docker Version & Info

```
docker --version
docker info
```

👉 Check Docker installation and system details

---

# 📌 2. Docker Pull (Download Image)

```
docker pull nginx
```

👉 Pull image from Docker Hub

---

# 📌 3. Docker Build (Create Image)

```
docker build -t myapp .
```

👉 Build image from Dockerfile

---

# 📌 4. Docker Images

```
docker images
```

👉 List all images

---

# 📌 5. Docker Run

Run container:

```
docker run -d -p 80:80 nginx
```

👉 Run container in detached mode

---

# 📌 6. Docker PS

```
docker ps
docker ps -a
```

👉 List running / all containers

---

# 📌 7. Docker Stop / Start

```
docker stop <container-id>
docker start <container-id>
```

👉 Manage container lifecycle

---

# 📌 8. Docker Exec (Access Container)

```
docker exec -it <container-id> /bin/bash
```

👉 Access running container

---

# 📌 9. Docker Logs

```
docker logs <container-id>
```

👉 View container logs (important for debugging)

---

# 📌 10. Docker Inspect

```
docker inspect <container-id>
```

👉 Detailed container info (IP, config, mounts)

---

# 📌 11. Docker Remove

Remove container:

```
docker rm <container-id>
```

Remove image:

```
docker rmi <image-id>
```

---

# 📌 12. Docker Network

List networks:

```
docker network ls
```

Create network:

```
docker network create mynetwork
```

Run container in network:

```
docker run --network=mynetwork nginx
```

👉 Used for container communication

---

# 📌 13. Docker Volume (Persistent Storage)

Create volume:

```
docker volume create myvolume
```

Use volume:

```
docker run -v myvolume:/data nginx
```

👉 Prevent data loss

---

# 📌 14. Docker Compose

Run multi-container app:

```
docker-compose up -d
```

Stop:

```
docker-compose down
```

👉 Manage multiple containers

---

# 📌 15. Docker Tag & Push

Tag image:

```
docker tag myapp:latest myrepo/myapp:latest
```

Push image:

```
docker push myrepo/myapp:latest
```

👉 Push to registry

---

# 📌 16. Docker Login

```
docker login
```

👉 Authenticate to Docker Hub / private registry

---

# 📌 17. Docker Stats

```
docker stats
```

👉 Monitor CPU, memory usage

---

# 📌 18. Docker Top

```
docker top <container-id>
```

👉 Show running processes inside container

---

# 📌 19. Docker Save & Load

Save image:

```
docker save -o myimage.tar myapp
```

Load image:

```
docker load -i myimage.tar
```

👉 Used for offline environments

---

# 📌 20. Docker Prune (Cleanup)

```
docker system prune -a
```

👉 Remove unused containers/images

---

# 🚀 DevOps Real Usage Examples

## CI/CD Pipeline Build & Push
```
docker build -t app .
docker tag app repo/app
docker push repo/app
```

---

## Debug Container Issue
```
docker logs <id>
docker exec -it <id> /bin/bash
```

---

## Multi-Container Setup
```
docker-compose up -d
```

---

## Resource Monitoring
```
docker stats
```

---

# 🎯 Why These Commands Are Important

DevOps engineers use Docker commands for:

- container deployment
- debugging issues
- CI/CD pipelines
- microservices architecture
- performance monitoring

Mastering these commands shows **real production-level experience**.
