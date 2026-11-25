# Docker Image Creation using Nginx

## Project Overview
This project demonstrates how to create a custom Docker image using an Nginx base image and deploy a simple HTML website inside a Docker container.

## Objectives
- Understand Docker images and containers.
- Write a Dockerfile.
- Build a custom Docker image.
- Run an Nginx container.
- Access a website through port mapping.

## Technologies Used
- Docker
- Nginx
- HTML
- RHEL 9.2

## Project Structure
```text
01-Docker-Image/
├── Dockerfile
├── index.html
├── .dockerignore
├── README.md
└── screenshots/
```

## Implementation Steps

### 1. Create the Dockerfile
The Dockerfile uses the official Nginx image, copies the HTML file into the Nginx web directory, and documents port 80.

### 2. Build the Docker Image
```bash
docker build -t my-docker-project:v1 .
```

### 3. Verify the Image
```bash
docker images
```

### 4. Run the Container
```bash
docker run -d --name my-website -p 8080:80 my-docker-project:v1
```

### 5. Verify the Container
```bash
docker ps
docker logs my-website
```

### 6. Test the Website
```bash
curl http://localhost:8080
```

Open `http://localhost:8080` in a browser on the VM, or use the VM IP with port 8080 from another machine.

## Result
Successfully built a custom Docker image and deployed an HTML website inside an Nginx container.

## What I Learned
- Dockerfile instructions: FROM, COPY, EXPOSE.
- Docker image creation.
- Container lifecycle basics.
- Port mapping between host and container.
- Deploying a website using Docker.
