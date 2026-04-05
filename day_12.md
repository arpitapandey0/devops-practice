# Docker Run Command

## Overview
The `docker run` command is used to create and start a container from a Docker image. It is one of the most commonly used Docker commands.

---

## Syntax
```
docker run [OPTIONS] IMAGE [COMMAND] [ARG...]
```

---

## Basic Example
```
docker run ubuntu
```

### Description
- Downloads the `ubuntu` image (if not already present)  
- Creates a container  
- Runs the default command  

---

## Common Options

### 1. Run in Detached Mode
```
docker run -d nginx
```
- Runs container in background  

---

### 2. Assign Name to Container
```
docker run --name mycontainer nginx
```

---

### 3. Port Mapping
```
docker run -p 8080:80 nginx
```
- Maps port 8080 (host) to port 80 (container)  

---

### 4. Interactive Mode
```
docker run -it ubuntu bash
```
- `-i` → Interactive  
- `-t` → Terminal  
- Opens shell inside container  

---

### 5. Environment Variables
```
docker run -e APP_ENV=production myapp
```

---

### 6. Mount Volume
```
docker run -v /host/path:/container/path nginx
```

---

### 7. Remove Container Automatically
```
docker run --rm ubuntu
```
- Deletes container after execution  

---

## How docker run Works

```
Check Image → Pull (if not present) → Create Container → Start Container
```

---

## Example Workflow
```
docker run -d -p 3000:3000 --name app myapp:v1
```

### This will:
- Run container in background  
- Map port 3000  
- Assign name "app"  
- Use image "myapp:v1"  

---

## Advantages

- Quick container creation  
- Flexible configuration options  
- Supports networking, storage, and environment setup  
- Essential for testing and deployment  

---

## Common Use Cases

- Running applications  
- Testing environments  
- Starting services (e.g., web servers, databases)  
- Debugging containers  

---

## Conclusion
The `docker run` command is a powerful and essential tool in Docker. It allows users to quickly create and manage containers with various configurations, making it fundamental for container-based workflows.

---

## References
- Docker Documentation  
