# Image Registries

## Overview
Image registries are storage and distribution systems for container images. They allow developers to store, manage, and share container images across different environments.

---

## What is an Image Registry?

An image registry is a centralized repository where container images are stored and accessed. It enables users to:
- Push (upload) images  
- Pull (download) images  
- Manage versions using tags  

---

## How Image Registries Work

```
Developer builds image
        ↓
Push image to registry
        ↓
Registry stores image
        ↓
User pulls image
        ↓
Run container
```

---

## Types of Image Registries

### 1. Public Registries
- Accessible to everyone  
- Used for sharing open-source images  

Examples:
- Docker Hub  
- GitHub Container Registry  

---

### 2. Private Registries
- Restricted access  
- Used within organizations  
- More secure for sensitive applications  

Examples:
- AWS Elastic Container Registry (ECR)  
- Google Container Registry (GCR)  
- Azure Container Registry (ACR)  

---

## Key Features

- Image storage and versioning  
- Access control and authentication  
- Image tagging and labeling  
- High availability  
- Integration with CI/CD pipelines  

---

## Image Tagging

Tags are used to identify versions of images.

### Example
```
myapp:latest
myapp:v1.0
myapp:v2.1
```

---

## Basic Commands (Docker)

### Login to Registry
```
docker login
```

### Push Image
```
docker push username/image:tag
```

### Pull Image
```
docker pull username/image:tag
```

---

## Advantages

- Centralized image management  
- Easy sharing and distribution  
- Version control using tags  
- Supports automation (CI/CD)  
- Improves deployment consistency  

---

## Disadvantages

- Security risks if not properly configured  
- Storage costs for private registries  
- Dependency on network availability  

---

## Best Practices

- Use private registries for sensitive data  
- Tag images properly (avoid only using "latest")  
- Regularly clean unused images  
- Enable authentication and access control  
- Scan images for vulnerabilities  

---

## Conclusion
Image registries are essential for managing and distributing container images. They play a key role in DevOps workflows by enabling efficient, secure, and scalable application deployment.

---

## References
- Docker Documentation  
- Kubernetes Documentation  
- AWS ECR Documentation  
