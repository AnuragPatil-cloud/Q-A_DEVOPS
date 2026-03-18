# 🐳 Docker Interview Questions & Answers (DevOps)

This section contains commonly asked **Docker interview questions** for DevOps engineers.

---

# 1. What is Docker?

Docker is an **open-source containerization platform that allows applications to run in isolated environments called containers**.

It ensures consistency across development, testing, and production environments.

---

# 2. What is a Container?

A container is a **lightweight, portable unit that includes an application and its dependencies**.

Containers share the host OS kernel but run in isolated environments.

---

# 3. What is a Docker Image?

A Docker image is a **read-only template used to create containers**.

It contains:

- application code
- dependencies
- configuration

---

# 4. What is the difference between Image and Container?

| Feature | Image | Container |
|---|---|---|
Nature | Template | Running instance |
State | Read-only | Read-write |
Usage | Used to create containers | Executes application |

---

# 5. What is a Dockerfile?

A Dockerfile is a **text file containing instructions to build a Docker image**.

Example:

```
FROM ubuntu
RUN apt update
CMD ["echo", "Hello DevOps"]
```

---

# 6. What is Docker Hub?

Docker Hub is a **public repository where Docker images are stored and shared**.

Users can:

- pull images
- push images
- share containers

---

# 7. What are common Docker commands?

Examples:

```
docker build -t myapp .
docker run -d -p 80:80 nginx
docker ps
docker stop <container-id>
docker rm <container-id>
```

---

# 8. What is Docker Volume?

Docker volumes are used to **persist data outside the container**.

This ensures data is not lost when containers are removed.

---

# 9. What is Docker Network?

Docker networking allows **communication between containers and external systems**.

Types of networks:

- bridge
- host
- overlay

---

# 10. What is Docker Compose?

Docker Compose is a tool used to **define and manage multi-container applications using a YAML file**.

Example:

```
version: '3'
services:
  web:
    image: nginx
  db:
    image: mysql
```

---

# 11. What is the difference between Docker and Virtual Machine?

| Feature | Docker | Virtual Machine |
|---|---|---|
Architecture | Container-based | Hypervisor-based |
Performance | Lightweight | Heavy |
Startup Time | Fast | Slow |

---

# 12. What is Docker Engine?

Docker Engine is the **core component that runs and manages Docker containers**.

It includes:

- Docker daemon
- REST API
- CLI

---

# 13. What is Docker Registry?

A Docker registry is a **storage system for Docker images**.

Examples:

- Docker Hub
- AWS ECR
- Google Container Registry

---

# 14. What is the use of EXPOSE in Dockerfile?

EXPOSE defines **which port the container listens on at runtime**.

Example:

```
EXPOSE 80
```

---

# 15. What is CMD vs ENTRYPOINT?

| CMD | ENTRYPOINT |
|---|---|
Provides default command | Defines fixed command |
Can be overridden | Hard to override |

---

# 16. What is Docker Layer?

Docker images are built using **layers**, where each instruction creates a new layer.

Benefits:

- faster builds
- caching
- efficient storage

---

# 17. What is a Multi-stage Build in Docker?

Multi-stage builds allow **creating smaller and optimized Docker images** by separating build and runtime environments.

---

# 18. What is Docker Swarm?

Docker Swarm is a **container orchestration tool used to manage multiple Docker nodes as a cluster**.

---

# 19. What are common Docker use cases?

- application deployment
- microservices architecture
- CI/CD pipelines
- environment consistency

---

# 20. Why is Docker important for DevOps?

Docker helps DevOps teams:

- package applications consistently
- reduce environment issues
- improve deployment speed
- support microservices architecture
