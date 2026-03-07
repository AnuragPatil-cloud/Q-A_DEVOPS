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
---
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
---
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
---
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
---
### What is a Docker container?
```
A Docker Container is a running instance of a Docker image.
 It is a lightweight, isolated environment where an application runs with all its dependencies. 🐳
Containers are created and managed using Docker.

Simple Definition
Docker Container = A running application created from a Docker image.
```
---
### What is Docker Hub?
```
Docker Hub is a cloud-based repository (registry) used to store, manage, and share Docker images.
It is the default image registry used by Docker. 🐳

Simple Definition
Docker Hub = Online registry where Docker images are stored and shared.
```
---
### What is Docker registry?
```
A Docker Registry is a storage and distribution system for Docker images.
It allows users to store, manage, and share Docker images so they can be downloaded and used to create containers. 🐳
Docker images are created and used by Docker.

Simple Definition
Docker Registry = A server or service that stores Docker images and allows users to push and pull them.
```
---
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
---
### What is Dockerfile?
```
A Dockerfile is a text file that contains a set of instructions used to build a Docker image automatically.
 It defines how the container environment should be created. 🐳
It is used by Docker to build images.

Simple Definition
Dockerfile = Script with instructions to create a Docker image.
```
---
### What are Docker layers?
```
Docker layers are the building blocks of a Docker image. Every instruction in a Dockerfile (like FROM, RUN, COPY)
creates a new layer in the image.
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
---
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
---
### What is Docker client?
```
The Docker Client is the command-line interface (CLI) or tool that you use to interact with Docker.
 It sends commands to the Docker Daemon, which then performs the requested actions. 🐳

Simple Definition
Docker Client = The interface (CLI) you use to communicate with the Docker Daemon to manage images, containers, networks, and volumes.
```
---
### Explain Docker architecture.
```
Docker Architecture has three main components:

1-Docker Client – User interface to interact with Docker
2-Docker Daemon – Background service that manages containers, images, networks, and volumes
3-Docker Objects – Images, Containers, Volumes, Networks

These components communicate to build, ship, and run applications inside containers.
[Docker Client]  --->  [Docker Daemon (dockerd)]  --->  [Containers / Images / Networks / Volumes]
        |                                         \
        |                                          ---> [Docker Registry (Docker Hub, ECR, GCR)]

Components Explained
1️⃣ Docker Client
The interface used to send commands to the Docker Daemon.
Commands can be:
docker build → build an image from a Dockerfile
docker run → run a container
docker pull → download an image from a registry

2️⃣ Docker Daemon (dockerd)
Runs as a background service on the host system.
Manages:
Images
Containers
Networks
Volumes
Listens to Docker Client requests and performs actions.

3️⃣ Docker Objects
Images – Read-only templates used to create containers
Containers – Running instances of images
Volumes – Persist data outside containers
Networks – Allow communication between containers

4️⃣ Docker Registry
Stores Docker images.
Examples:
Public: Docker Hub
Private: Amazon Elastic Container Registry, Google Container Registry
```
---
### What is the difference between COPY and ADD?
```
In Dockerfiles, both COPY and ADD are used to move files from the host machine into a Docker image, but they have important differences.
 This is a very common Docker interview question. 🐳

| Instruction | Purpose                                                                                                                  |
| ----------- | ------------------------------------------------------------------------------------------------------------------------ |
| **COPY**    | Copies files or directories from the host into the Docker image. Simple and straightforward.                             |
| **ADD**     | Copies files or directories from host **and can also fetch files from URLs** and extract compressed files automatically. |

| Feature         | COPY                     | ADD                                                 |
| --------------- | ------------------------ | --------------------------------------------------- |
| Source          | Local files only         | Local files or remote URL                           |
| Functionality   | Copies files/directories | Copies + extracts tar files + fetches remote files  |
| Complexity      | Simple and predictable   | More complex; can have unintended effects           |
| Recommended Use | For normal copying       | Only when you need `tar` extraction or URL fetching |

Examples
Using COPY
COPY ./app /app
Copies the app folder from your host to /app inside the image.

Using ADD
ADD https://example.com/app.tar.gz /app/
Downloads the tarball from the URL and extracts it into /app/ automatically.
Or from local:
ADD app.tar.gz /app/
Extracts the tarball automatically.
```
---
### Difference between CMD and ENTRYPOINT?
```
In Dockerfiles, both CMD and ENTRYPOINT specify what command runs when a container starts, but they behave differently.
 This is a very common Docker interview question. 🐳

1. Basic Definitions
| Instruction    | Purpose                                                                                   |
| -------------- | ----------------------------------------------------------------------------------------- |
| **CMD**        | Provides **default command and arguments** for a container. Can be overridden at runtime. |
| **ENTRYPOINT** | Configures a container to **run as an executable**, making it hard to override.           |

2. Key Differences
| Feature  | CMD                                          | ENTRYPOINT                                      |
| -------- | -------------------------------------------- | ----------------------------------------------- |
| Override | Can be overridden at `docker run`            | Harder to override, unless using `--entrypoint` |
| Purpose  | Default command                              | Defines main command for the container          |
| Syntax   | Shell form or exec form                      | Shell form or exec form                         |
| Use Case | For **default behavior** that can be changed | For **container as a specific application**     |


3. Syntax Examples
Using CMD
FROM ubuntu
CMD ["echo", "Hello World"]
Default: prints Hello World

Can be overridden:
docker run myimage echo "Hi Docker"

Using ENTRYPOINT
FROM ubuntu
ENTRYPOINT ["echo"]
Default: echo is fixed
Arguments can be appended at runtime:
docker run myimage "Hello Docker"
# Output: Hello Docker
Hard to change echo without --entrypoint

4. Combining ENTRYPOINT and CMD
You can combine both:
FROM ubuntu
ENTRYPOINT ["echo"]
CMD ["Hello World"]
By default: prints Hello World

You can override CMD arguments:
docker run myimage "Docker Rocks"
# Output: Docker Rocks
```
---
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
