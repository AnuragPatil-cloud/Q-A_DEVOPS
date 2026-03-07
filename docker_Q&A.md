# Docker Interview Questions (30)

### 1. What is Docker?
```
  Docker is a containerization platform used to build, package, and run applications in containers. 🐳
A container is a lightweight package that includes:
-Application code
-Runtime
-Libraries
-Dependencies
-System tools
Because everything needed is inside the container,
the application runs the same way on any machine (developer laptop, server, cloud, etc.)
```
### 2. What is containerization?
```
Containerization is a technology used to package an application along with all its dependencies, libraries,
and configuration files into a single unit called a container so that it runs consistently across different environments. 📦🐳
*Why Containerization is Needed:
Sometimes an application works on a developer's laptop but fails on the server because of:
-Different OS
-Missing libraries
-Different runtime versions
Containerization solves this problem by packaging everything required to run the application.
```
### 3. Difference between Docker and Virtual Machine?
```
# Docker (Containers)
-Lightweight virtualization technology.
-Packages application + dependencies into containers.
-Containers share the host operating system kernel.

# Virtual Machine (VM)
-Full virtualization technology.
-Runs a complete operating system on top of a hypervisor.
```
### What is a Docker image?
```
A Docker Image is a read-only template used to create Docker containers.
 It contains everything needed to run an application.
It includes:
Application code
Runtime (Java, Python, Node.js, etc.)
Libraries
Dependencies
Environment variables
Configuration files
Docker images are used by Docker to create and run containers.

Simple Definition
Docker Image = Blueprint or template used to create Docker containers.
```
### What is a Docker container?
```
A Docker Container is a running instance of a Docker image.
 It is a lightweight, isolated environment where an application runs with all its dependencies. 🐳
Containers are created and managed using Docker.

Simple Definition
Docker Container = A running application created from a Docker image.
```

### What is Docker Hub?
```
Docker Hub is a cloud-based repository (registry) used to store, manage, and share Docker images.
It is the default image registry used by Docker. 🐳

Simple Definition
Docker Hub = Online registry where Docker images are stored and shared.
```

### What is Docker registry?
```
A Docker Registry is a storage and distribution system for Docker images.
It allows users to store, manage, and share Docker images so they can be downloaded and used to create containers. 🐳
Docker images are created and used by Docker.

Simple Definition
Docker Registry = A server or service that stores Docker images and allows users to push and pull them.
```

### Difference between Docker image and container?
```
The difference between a Docker Image and a Docker Container is that an image is a template,
while a container is a running instance of that template. Both are core components of Docker. 🐳

| Feature   | Docker Image              | Docker Container                   |
| --------- | ------------------------- | ---------------------------------- |
| Type      | Template                  | Running instance                   |
| State     | Static                    | Running / Dynamic                  |
| Editable  | Read-only                 | Writable layer                     |
| Purpose   | Used to create containers | Runs the application               |
| Lifecycle | Built once                | Created, started, stopped, deleted |
```

### What is Dockerfile?
```
A Dockerfile is a text file that contains a set of instructions used to build a Docker image automatically.
 It defines how the container environment should be created. 🐳
It is used by Docker to build images.

Simple Definition
Dockerfile = Script with instructions to create a Docker image.
```

### What are Docker layers?
```
Docker layers are the building blocks of a Docker image. Every instruction in a Dockerfile (like FROM, RUN, COPY) creates a new layer in the image.
These layers make Docker images efficient, reusable, and lightweight. 🐳

Simple Definition
Docker layers = Read-only filesystem snapshots created for each instruction in a Dockerfile.
They are stacked to form a complete Docker image.

How Layers Work
Each Dockerfile instruction creates a layer.
Layers are cached. If nothing changes in a layer, Docker reuses it during the next build.
Layers are stacked on top of each other to form the final image.

Example

Dockerfile:
FROM ubuntu:22.04
RUN apt-get update
RUN apt-get install -y python3
COPY app.py /app/
CMD ["python3", "/app/app.py"]

Layers created:

FROM ubuntu:22.04 → Base OS layer
RUN apt-get update → Update layer
RUN apt-get install -y python3 → Python installation layer
COPY app.py /app/ → Application layer
CMD ["python3", "/app/app.py"] → Command layer
Each layer is read-only, except the container’s writable layer when running.
```

### What is Docker daemon?
```
The Docker Daemon is the background service that runs on your system and manages Docker objects, such as images, containers, networks, and volumes.
 It is a core component of Docker. 🐳

Simple Definition

Docker Daemon = The background service that listens for Docker commands and manages Docker containers and images.
Key Points

Runs in the background
On Linux: dockerd
On Windows/Mac: Runs inside Docker Desktop

Manages Docker objects
Containers,Images,Networks,Volumes,Communicates with Docker client

The Docker CLI (docker run, docker build) sends commands to the daemon via REST API.
How It Works
Docker Client  →  REST API  →  Docker Daemon → Manages Containers & Images

```

What is Docker client?

Explain Docker architecture.

What is the difference between COPY and ADD?

Difference between CMD and ENTRYPOINT?

What is Docker volume?

Why do we use Docker volumes?

What is Docker networking?

Types of Docker networks?

What is bridge network?

What is host network?

What is Docker Compose?

What is multi-stage build?

How to reduce Docker image size?

What is .dockerignore?

How do containers communicate?

What happens when a container crashes?

What is Docker Swarm?

How to check container logs?

Difference between Docker run and Docker start?
