# Docker -p (Port Mapping)

## Overview
The `-p` option in Docker is used to map ports between the host machine and a container. It allows external users or systems to access services running inside a container.

---

## Syntax
```
docker run -p HOST_PORT:CONTAINER_PORT IMAGE
```

---

## Example
```
docker run -p 8080:80 nginx
```

### Explanation
- `8080` → Port on the host machine  
- `80` → Port inside the container  
- `nginx` → Image running a web server  

Access the application in browser:
```
http://localhost:8080
```

---

## How It Works

```
User Request → Host Port (8080) → Container Port (80) → Application
```

---

## Multiple Port Mapping

```
docker run -p 8080:80 -p 3000:3000 myapp
```

---

## Run in Background with Port Mapping

```
docker run -d -p 8080:80 nginx
```

---

## Binding to Specific IP

```
docker run -p 127.0.0.1:8080:80 nginx
```

- Only accessible from localhost  

---

## Exposing Ports vs Publishing Ports

- `EXPOSE` (in Dockerfile)
  - Documentation purpose  
  - Does not publish the port  

- `-p`
  - Actually maps and makes the port accessible  

---

## Advantages

- Enables external access to containerized applications  
- Supports web servers, APIs, and databases  
- Flexible port configuration  
- Allows multiple services on different ports  

---

## Disadvantages

- Port conflicts if already in use  
- Security risk if exposed publicly  
- Requires proper configuration  

---

## Common Use Cases

- Running web servers (nginx, apache)  
- Hosting APIs  
- Testing applications locally  
- Connecting to databases  

---

## Conclusion
The `-p` option is essential for exposing container services to the outside world. It bridges the gap between the host system and containerized applications, making them accessible and usable.

---

## References
- Docker Documentation  
