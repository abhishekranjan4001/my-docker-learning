# 🐳 Docker Commands Guide  

## 📌 1. Docker Version & Info  
Check if Docker is installed and running:  
```sh
docker --version       # Show installed Docker version  
docker info            # Display system-wide information  
```

## 📌 2. Working with Images  
### 🔍 Search for an Image  
```sh
docker search ubuntu   # Search for images on Docker Hub  
```

### 👥 Pull an Image  
```sh
docker pull ubuntu     # Download an image from Docker Hub  
```

### 📝 List Downloaded Images  
```sh
docker images          # List all local Docker images  
```

### 🗑️ Remove an Image  
```sh
docker rmi ubuntu      # Remove an image  
docker rmi $(docker images -q)  # Remove all images  
```

## 📌 3. Working with Containers  
### 🚀 Run a Container  
```sh
docker run ubuntu      # Run a container using the Ubuntu image  
docker run -it ubuntu  # Run an interactive shell inside the container  
```

### 📝 List Running Containers  
```sh
docker ps             # Show running containers  
docker ps -a          # Show all containers (including stopped ones)  
```

### 😑 Stop & Remove Containers  
```sh
docker stop <container_id>      # Stop a running container  
docker rm <container_id>        # Remove a stopped container  
docker rm $(docker ps -aq)      # Remove all stopped containers  
```

## 📌 4. Working with Container Logs & Processes  
### 📝 View Container Logs  
```sh
docker logs <container_id>     # Show logs of a running container  
```

### 🔎 Inspect Container Details  
```sh
docker inspect <container_id>  # Get low-level information about a container  
```

### 📌 Execute Commands Inside a Running Container  
```sh
docker exec -it <container_id> bash   # Open a bash shell in the container  
docker exec <container_id> ls         # Run a command inside the container  
```

## 📌 5. Docker Networking  
### 🌐 List Networks  
```sh
docker network ls     # List all Docker networks  
```

### 🔗 Create a New Network  
```sh
docker network create my_network  
```

### 🌿 Connect a Container to a Network  
```sh
docker network connect my_network <container_id>  
```

## 📌 6. Docker Volumes (Persistent Storage)  
### 📝 List Volumes  
```sh
docker volume ls      # Show all Docker volumes  
```

### 📂 Create a Volume  
```sh
docker volume create my_volume  
```

### 🚀 Use a Volume in a Container  
```sh
docker run -v my_volume:/data ubuntu  
```

### 🗑️ Remove a Volume  
```sh
docker volume rm my_volume  
```

## 📌 7. Building & Managing Docker Images  
### 🏢 Build a Docker Image  
```sh
docker build -t my_app .  
```

### 👥 Tag an Image  
```sh
docker tag my_app myrepo/my_app:v1  
```

### 💌 Push an Image to Docker Hub  
```sh
docker push myrepo/my_app:v1  
```

## 📌 8. Docker Compose Commands  
### 🚀 Start Services Defined in `docker-compose.yml`  
```sh
docker-compose up      # Start services  
docker-compose up -d   # Start in detached mode  
```

### 🚫 Stop Services  
```sh
docker-compose down    # Stop and remove services  
```

### 📝 View Logs  
```sh
docker-compose logs    # View logs for all services  
```

## 📌 9. Docker System Cleanup  
### 🗑️ Remove Unused Data  
```sh
docker system prune   # Remove unused containers, images, and networks  
```

### 🚀 Free Up Disk Space  
```sh
docker system df      # Show Docker disk usage  
```

## 🎯 Conclusion  
These commands will help you **effectively manage Docker images, containers, networks, and volumes**. Keep this guide handy as a **quick reference**! 🚀🐳  

