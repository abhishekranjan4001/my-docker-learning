# Installing Docker  

## 🏗️ Install Docker on Windows, Mac, and Linux  

### **Windows**
1. Download **Docker Desktop** from [Docker Official Website](https://www.docker.com/products/docker-desktop).
2. Run the installer and follow the instructions.
3. Enable **WSL 2 Backend** (if prompted).
4. Restart your computer if required.
5. Verify installation:  
   ```sh
   docker --version
   ```

### **Mac**
1. Download **Docker Desktop for Mac** from [Docker Official Website](https://www.docker.com/products/docker-desktop).
2. Open the downloaded `.dmg` file and drag Docker to the Applications folder.
3. Launch Docker Desktop.
4. Verify installation:  
   ```sh
   docker --version
   ```

### **Linux (Ubuntu/Debian-based Distros)**
1. Update the package database:
   ```sh
   sudo apt update
   sudo apt install -y ca-certificates curl gnupg
   ```
2. Add Docker's official GPG key:
   ```sh
   sudo install -m 0755 -d /etc/apt/keyrings
   curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo tee /etc/apt/keyrings/docker.asc > /dev/null
   sudo chmod a+r /etc/apt/keyrings/docker.asc
   ```
3. Add Docker repository:
   ```sh
   echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
   ```
4. Install Docker:
   ```sh
   sudo apt update
   sudo apt install -y docker-ce docker-ce-cli containerd.io
   ```
5. Verify installation:
   ```sh
   docker --version
   ```

### **Linux (CentOS/RHEL-based Distros)**
1. Install required packages:
   ```sh
   sudo yum install -y yum-utils
   ```
2. Add Docker repository:
   ```sh
   sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo
   ```
3. Install Docker:
   ```sh
   sudo yum install -y docker-ce docker-ce-cli containerd.io
   ```
4. Start Docker service:
   ```sh
   sudo systemctl start docker
   sudo systemctl enable docker
   ```
5. Verify installation:
   ```sh
   docker --version
   ```

### **Post-Installation Steps for Linux**
To run Docker without `sudo`:
```sh
sudo groupadd docker
sudo usermod -aG docker $USER
newgrp docker
```

✅ Docker is now installed on your system! 🎉
