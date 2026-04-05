# Docker Commands: version, info, history, images

## Overview
Docker provides various commands to inspect system details, images, and their history. These commands are essential for debugging, monitoring, and managing containerized applications.

---

## 1. Docker Version

### Command
```
docker version
```

### Description
Displays the installed Docker version details for both:
- Client  
- Server (Docker Daemon)  

### Output Includes
- Version number  
- API version  
- Go version  
- Git commit  
- Build time  

---

## 2. Docker Info

### Command
```
docker info
```

### Description
Provides detailed information about the Docker system.

### Output Includes
- Number of containers (running, paused, stopped)  
- Number of images  
- Storage driver  
- CPU and memory details  
- Docker root directory  
- Operating system  

---

## 3. Docker Images

### Command
```
docker images
```

### Description
Lists all Docker images available on the local system.

### Output Columns
- Repository  
- Tag  
- Image ID  
- Created  
- Size  

### Example
```
REPOSITORY   TAG       IMAGE ID       CREATED        SIZE
ubuntu       latest    abc123         2 days ago     72MB
```

---

## 4. Docker History

### Command
```
docker history <image_name>
```

### Description
Shows the history of an image, including all layers used to build it.

### Output Includes
- Layer creation time  
- Commands used  
- Size of each layer  

### Example
```
docker history ubuntu
```

---

## Use Cases

- `docker version` → Check installed Docker version  
- `docker info` → Get system-level details  
- `docker images` → View available images  
- `docker history` → Analyze image layers  

---

## Advantages

- Helps in debugging issues  
- Provides system insights  
- Useful for image optimization  
- Easy monitoring of Docker environment  

---

## Conclusion
These Docker commands are essential for managing and understanding Docker environments. They help developers inspect system configurations, monitor images, and analyze image structures effectively.

---

## References
- Docker Documentation  
