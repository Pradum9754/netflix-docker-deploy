# netflix-docker-deploy
Dockerized Netflix-style streaming application deployed on cloud VM with Nginx — fully containerized and production-ready.

# Netflix Docker Deployment

This repository contains a **Dockerized Netflix-style streaming application** deployed on a cloud VM using Nginx.

## Features

- Runs on **Nginx** with clean deployment
- Full **Docker containerization**
- Easy to build and run locally or on cloud
- Includes a **ready-to-use Dockerfile**

## Dockerfile

```dockerfile
FROM nginx:latest
EXPOSE 80
RUN rm -rf /usr/share/nginx/html/*
COPY . /usr/share/nginx/html
Build & Run

Build the Docker image:

docker build -t netflix:nginx .


Run the container:

docker run -d -p 80:80 netflix:nginx


Access the app at: http://<VM_IP>

Project Structure
StreamFlix/
├── Dockerfile
├── index.html
├── css/
└── js/


(Replace index.html, css/, js/ with your StreamFlix app content)

Notes

Ensure Docker is installed on your system

Current deployment uses Nginx to serve the app

Can be extended to multi-container setup with Docker Compose

License

MIT License
