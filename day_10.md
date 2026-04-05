# Docker Architecture and Lifecycle

## Overview
Docker is a containerization platform that enables developers to build, ship, and run applications in containers. Understanding its architecture and lifecycle is essential for working with containerized applications.

---

## Docker Architecture

Docker follows a client-server architecture.

### Components of Docker Architecture

### 1. Docker Client
- The interface used by users to interact with Docker  
- Executes commands like `docker build`, `docker run`, `docker pull`  
- Communicates with Docker Daemon  

---

### 2. Docker Daemon (dockerd)
- Runs on the host machine  
- Responsible for managing containers, images, networks, and volumes  
- Listens for Docker API requests  

---

### 3. Docker Images
- Read-only templates used to create containers  
- Built using Dockerfile  

---

### 4. Docker Containers
- Running instances of Docker images  
- Lightweight and isolated environments  

---

### 5. Docker Registry
- Stores Docker images  
- Example: Docker Hub  

---

## Architecture Diagram

```
Docker Client
      ↓
Docker Daemon (dockerd)
      ↓
---------------------------------
|   Images   |   Containers      |
---------------------------------
      ↓
Docker Registry (Docker Hub)
```

---

## Docker Lifecycle

The Docker lifecycle represents the stages from image creation to container execution.

### 1. Build
- Create an image using a Dockerfile  
```
docker build -t myapp .
```

---

### 2. Pull
- Download an image from a registry  
```
docker pull ubuntu
```

---

### 3. Run
- Create and start a container  
```
docker run -d myapp
```

---

### 4. Stop
- Stop a running container  
```
docker stop <container_id>
```

---

### 5. Start
- Restart a stopped container  
```
docker start <container_id>
```

---

### 6. Remove
- Delete container or image  
```
docker rm <container_id>
docker rmi <image_id>
```

---

### 7. Push
- Upload image to registry  
```
docker push username/myapp:v1
```

---

## Lifecycle Flow

```
Dockerfile → Build Image → Push/Pull Image → Run Container → Stop/Start → Remove
```

---

## Advantages of Docker Architecture

- Lightweight and fast  
- Scalable and portable  
- Efficient resource usage  
- Supports microservices architecture  

---

## Conclusion
Docker architecture uses a client-server model to manage containers efficiently. Its lifecycle simplifies application development, deployment, and scaling, making it a key tool in DevOps and cloud environments.

---

## References
- Docker Documentation  
- Docker Hub Documentation  
