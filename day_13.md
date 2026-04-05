# Setting Up Environment Variables in Docker

## Overview
Environment variables in Docker are used to configure applications dynamically without modifying the code. They are commonly used for storing configuration values such as database URLs, API keys, and environment modes.

---

## Methods to Set Environment Variables

### 1. Using `-e` Flag (Command Line)

#### Syntax
```
docker run -e KEY=value IMAGE
```

#### Example
```
docker run -e APP_ENV=production ubuntu
```

### Multiple Variables
```
docker run -e APP_ENV=production -e DB_HOST=localhost ubuntu
```

---

### 2. Using `--env-file`

#### Step 1: Create `.env` file
```
APP_ENV=production
DB_HOST=localhost
PORT=3000
```

#### Step 2: Run container
```
docker run --env-file .env ubuntu
```

---

### 3. Using Dockerfile (`ENV` instruction)

#### Example Dockerfile
```
FROM ubuntu
ENV APP_ENV=production
ENV PORT=3000
```

---

### 4. Using Docker Compose

#### Example `docker-compose.yml`
```
version: '3'
services:
  app:
    image: myapp
    environment:
      - APP_ENV=production
      - PORT=3000
```

---

## Accessing Environment Variables Inside Container

### Example (Linux)
```
echo $APP_ENV
```

---

## Best Practices

- Do not hardcode sensitive data (use secrets instead)  
- Use `.env` files for better management  
- Keep environment-specific configurations separate  
- Use meaningful variable names  
- Avoid committing `.env` files to version control  

---

## Advantages

- Flexible configuration  
- Easy to modify without rebuilding images  
- Supports different environments (dev, test, prod)  
- Improves application portability  

---

## Disadvantages

- Security risks if sensitive data is exposed  
- Hard to manage at scale without proper tools  
- Requires careful handling in production  

---

## Conclusion
Environment variables in Docker provide a simple and effective way to manage application configuration. They help maintain flexibility, improve portability, and support modern DevOps practices.

---

## References
- Docker Documentation  
