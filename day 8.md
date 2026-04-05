# Tags and Versioning in Container Images

## Overview
Tags and versioning are used in container images to identify and manage different versions of an application. They help in tracking changes, ensuring consistency, and enabling reliable deployments.

---

## What are Tags?

Tags are labels assigned to container images to differentiate between versions.

### Example
```
myapp:latest
myapp:v1.0
myapp:v2.1
```

- `myapp` → Image name  
- `v1.0`, `latest` → Tags  

---

## Importance of Tags

- Identify specific versions of an image  
- Enable rollback to previous versions  
- Support continuous integration and deployment  
- Avoid confusion between different builds  

---

## What is Versioning?

Versioning is the practice of assigning meaningful version numbers to images to track changes over time.

---

## Types of Versioning

### 1. Semantic Versioning (SemVer)

Format:
```
MAJOR.MINOR.PATCH
```

### Meaning
- MAJOR → Breaking changes  
- MINOR → New features (backward compatible)  
- PATCH → Bug fixes  

### Example
```
v1.0.0 → Initial release  
v1.1.0 → Added new feature  
v1.1.1 → Bug fix  
v2.0.0 → Breaking changes  
```

---

### 2. Latest Tag

```
myapp:latest
```

- Refers to the most recent version  
- Not fixed or reliable  
- Can change over time  

---

### 3. Custom Tags

Used for specific environments or builds:
```
myapp:dev
myapp:test
myapp:prod
```

---

### 4. Commit-based Tags

```
myapp:abc123
```

- Based on Git commit IDs  
- Useful for tracking exact builds  

---

## Best Practices

- Avoid relying only on `latest`  
- Use semantic versioning for clarity  
- Tag images with both version and environment if needed  
- Maintain consistency in naming conventions  
- Keep old versions for rollback  

---

## Common Commands (Docker)

### Tag an Image
```
docker tag myapp:latest myapp:v1.0
```

### Push Tagged Image
```
docker push myapp:v1.0
```

---

## Advantages

- Better version control  
- Easy rollback to stable versions  
- Improved deployment reliability  
- Clear tracking of changes  

---

## Disadvantages

- Poor tagging can create confusion  
- Requires proper management and discipline  

---

## Conclusion
Tags and versioning are essential for managing container images effectively. They ensure consistency, traceability, and reliability in modern application deployment and DevOps workflows.

---

## References
- Docker Documentation  
- Semantic Versioning (semver.org)  
