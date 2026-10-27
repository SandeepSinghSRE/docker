# docker
# Docker Learning – Node.js Application

A beginner-friendly project to learn Docker step by step using Node.js, Ubuntu on WSL, Git, and GitHub.

## 🚀 Project Overview

This project runs a simple HTTP API inside a Docker container. It demonstrates how to build a Docker image, run a container, expose application ports, and manage containers.

## 🛠️ Technologies Used

- **Node.js** – JavaScript runtime
- **Docker Engine** – Containerization platform
- **Dockerfile** – Instructions to build the image
- **Git** – Version control
- **GitHub** – Remote repository
- **Ubuntu on WSL** – Linux development environment

## 📁 Project Structure

```text
docker-learning/
├── app.js
├── Dockerfile
├── .dockerignore
└── README.md
```

## ⚙️ Prerequisites

- Windows with WSL 2
- Ubuntu installed on WSL
- Git installed
- Docker Engine installed and running

Verify your installations:

```bash
git --version
docker --version
docker compose version
sudo docker info
```

## 🏗️ Build the Docker Image

Run this command from the project directory:

```bash
sudo docker build -t docker-learning:1.0 .
```

## ▶️ Run the Container

```bash
sudo docker run -d \
  --name docker-learning-app \
  -p 3000:3000 \
  docker-learning:1.0
```

## 🌐 Test the Application

Open this URL in your browser:

http://localhost:3000

Or run:

```bash
curl http://localhost:3000
```

Expected response:

```json
{
  "message": "Hello from Docker!",
  "path": "/"
}
```

## 🐳 Useful Docker Commands

Check running containers:

```bash
sudo docker ps
```

List all containers:

```bash
sudo docker ps -a
```

List images:

```bash
sudo docker images
```

View application logs:

```bash
sudo docker logs docker-learning-app
```

Stop the container:

```bash
sudo docker stop docker-learning-app
```

Start the container again:

```bash
sudo docker start docker-learning-app
```

Remove the container:

```bash
sudo docker rm -f docker-learning-app
```

## 🔄 Rebuild After Code Changes

After modifying `app.js`, rebuild the
