# Docker Environment Variable Example

## Objective
Run an Ubuntu container, set an environment variable, verify it, and observe its behavior after stopping and restarting the container.

---

## Step 1: Run Ubuntu Container with Environment Variable

```
docker run -it --name myubuntu -e COLLEGE=CSE ubuntu bash
```

### Description
- `-it` → Interactive terminal  
- `--name myubuntu` → Assigns container name  
- `-e COLLEGE=CSE` → Sets environment variable  
- `ubuntu` → Base image  
- `bash` → Opens shell  

---

## Step 2: Verify Environment Variable

Inside the container:
```
echo $COLLEGE
```

### Output
```
CSE
```

---

## Step 3: Stop the Container

Exit from container:
```
exit
```

OR stop using:
```
docker stop myubuntu
```

---

## Step 4: Restart the Container

```
docker start -ai myubuntu
```

Check again:
```
echo $COLLEGE
```

### Observation
The output will still be:
```
CSE
```

---

## Step 5: Remove Container and Check Again

Remove container:
```
docker rm myubuntu
```

Run a new container:
```
docker run -it ubuntu bash
```

Check variable:
```
echo $COLLEGE
```

### Output
```
(empty)
```

---

## Conclusion

- Environment variables set using `-e`:
  - Persist after container restart  
  - Do not persist after container deletion  

- They are stored in the container configuration, not in the image.

---

## Key Learning

- Use `-e` for runtime configuration  
- Use Dockerfile `ENV` if variables should persist in the image  
