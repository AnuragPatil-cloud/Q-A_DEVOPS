# 🐳 Docker Scenario-Based DevOps Interview Questions

This section contains **real-world Docker troubleshooting scenarios** commonly faced by DevOps engineers.

---

# Scenario 1: Docker Container Not Starting

### Problem
Container exits immediately after starting.

### Possible Causes

- application error
- incorrect CMD or ENTRYPOINT
- missing dependencies

### Solution

Check container logs:

```
docker logs <container-id>
```

Verify Dockerfile configuration and fix application errors.

---

# Scenario 2: Container Keeps Restarting

### Problem
Container goes into restart loop.

### Cause

Application crashing or health check failure.

### Solution

Check logs:

```
docker logs <container-id>
```

Inspect container:

```
docker inspect <container-id>
```

Fix application or configuration issue.

---

# Scenario 3: Port Not Accessible

### Problem
Application running inside container but not accessible externally.

### Possible Causes

- port not exposed
- incorrect port mapping
- firewall blocking

### Solution

Run container with port mapping:

```
docker run -d -p 8080:80 nginx
```

Verify port using:

```
docker ps
```

---

# Scenario 4: Image Build Failing

### Problem
Docker image build fails.

### Possible Causes

- syntax error in Dockerfile
- missing dependencies
- incorrect base image

### Solution

Check build logs:

```
docker build -t myapp .
```

Fix Dockerfile errors.

---

# Scenario 5: Data Lost After Container Restart

### Problem
Data inside container is lost after restart.

### Cause

Data stored inside container filesystem.

### Solution

Use Docker volumes:

```
docker run -v myvolume:/data
```

Volumes persist data outside container.

---

# Scenario 6: Container Cannot Connect to Another Container

### Problem
Two containers cannot communicate.

### Cause

Containers are not in same network.

### Solution

Create custom network:

```
docker network create mynetwork
```

Run containers in same network:

```
docker run --network mynetwork ...
```

---

# Scenario 7: High CPU or Memory Usage

### Problem
Container consuming too many resources.

### Solution

Limit resources:

```
docker run --memory="512m" --cpus="1"
```

Monitor usage:

```
docker stats
```

---

# Scenario 8: Cannot Pull Image from Registry

### Problem
Image pull fails.

### Possible Causes

- incorrect image name
- authentication issue
- network issue

### Solution

Login to registry:

```
docker login
```

Verify image name and connectivity.

---

# Scenario 9: Container Not Updating After Image Change

### Problem
New image changes not reflected in running container.

### Cause

Old container still running.

### Solution

Stop and remove container:

```
docker stop <id>
docker rm <id>
```

Run new container with updated image.

---

# Scenario 10: Need Multi-Container Setup

### Problem
Application has multiple services (web + database).

### Solution

Use Docker Compose.

Example:

```
version: '3'
services:
  web:
    image: nginx
  db:
    image: mysql
```

Run:

```
docker-compose up -d
```

---

# 🎯 Why Docker Scenarios Are Important for DevOps

DevOps engineers use Docker daily for:

- container deployment
- troubleshooting failures
- managing microservices
- optimizing performance
- ensuring application consistency

Understanding these scenarios helps maintain **reliable containerized applications in production**.
