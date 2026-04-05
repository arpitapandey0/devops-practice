# Container Images

## Overview
Container images are the foundation of containerization. They are lightweight, standalone, and executable packages that include everything needed to run an application, such as code, runtime, libraries, and dependencies.

---

## What is a Container Image?

A container image is a read-only template used to create containers. It contains:
- Application code  
- System libraries  
- Dependencies  
- Configuration files  

Containers are created as running instances of these images.

---

## Key Characteristics

- Lightweight compared to virtual machine images  
- Portable across different environments  
- Immutable (cannot be changed once built)  
- Layered structure for efficiency  

---

## How Container Images Work

```
Container Image (Read-only)
          ↓
   Container (Running Instance)
```

Each time an image is executed, a new container is created by adding a writable layer on top of the image.

---

## Image Layers

Container images are built in layers:
- Each layer represents a set of changes  
- Layers are cached and reused  
- Improves build speed and storage efficiency  

### Example
```
Base OS Layer
     ↓
Dependencies Layer
     ↓
Application Code Layer
     ↓
Configuration Layer
```

---

## Image Creation

Images are typically created using a **Dockerfile**, which contains instructions to build the image.

### Example Dockerfile
```
FROM ubuntu:latest
RUN apt-get update
RUN apt-get install -y python3
COPY . /app
CMD ["python3", "app.py"]
```

---

## Image Registry

Container images are stored and shared through registries.

### Types of Registries
- Public Registry (e.g., Docker Hub)  
- Private Registry (for organizations)  

---

## Image Lifecycle

1. Build the image  
2. Tag the image  
3. Push to registry  
4. Pull from registry  
5. Run as a container  

---

## Advantages

- Easy to distribute applications  
- Consistent runtime environment  
- Faster deployment  
- Reusability through layers  
- Version control with tags  

---

## Disadvantages

- Large images can increase storage usage  
- Security risks if images are not properly managed  
- Requires proper versioning and maintenance  

---

## Best Practices

- Use minimal base images  
- Reduce number of layers  
- Avoid unnecessary packages  
- Regularly update images  
- Scan images for vulnerabilities  

---

## Conclusion
Container images are essential for building and running containers. They ensure consistency, portability, and efficiency in modern application deployment.

---

## References
- Docker Documentation  
- Kubernetes Documentation  
