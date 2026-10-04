# 🚀 Task 1 — CI/CD Pipeline using GitHub Actions & Docker

## 📌 Project Overview

This project demonstrates a simple CI/CD pipeline for a Node.js application using GitHub Actions and Docker.

Whenever code is pushed to the `main` branch, GitHub Actions automatically runs the pipeline, tests the application, builds a Docker image, and pushes it to Docker Hub.

## 🛠️ Technologies Used

- Node.js
- Express.js
- Git & GitHub
- GitHub Actions
- Docker
- Docker Hub

## 🔄 CI/CD Workflow

Developer → Git Push → GitHub → GitHub Actions → Test → Docker Build → Docker Hub

## 📂 Project Structure

ci-cd-nodejs-app/
│
├── .github/
│   └── workflows/
│       └── main.yml
│
├── Dockerfile
├── .dockerignore
├── .gitignore
├── package.json
├── package-lock.json
└── server.js

## ⚙️ GitHub Actions

The workflow file is:

`.github/workflows/main.yml`

It runs automatically when code is pushed to the `main` branch.

The pipeline performs these steps:

1. Checkout the code from GitHub.
2. Setup Node.js.
3. Install dependencies using `npm ci`.
4. Run tests using `npm test`.
5. Build the Docker image.
6. Login to Docker Hub securely.
7. Push the Docker image to Docker Hub.

## 🐳 Docker

Build the Docker image:

`docker build -t ci-cd-nodejs-app:latest .`

Run the application:

`docker run -p 3000:3000 ci-cd-nodejs-app:latest`

## 🌐 Application

The application runs on port `3000`.

Home page:

`http://localhost:3000`

Response:

`Hello! My CI/CD Pipeline is working 🚀`

Health check:

`http://localhost:3000/health`

Response:

`{"status":"OK"}`

## 🔐 GitHub Secrets

Docker Hub credentials are stored securely in GitHub Repository Secrets:

- `DOCKERHUB_USERNAME`
- `DOCKERHUB_TOKEN`

These secrets are used by GitHub Actions to login to Docker Hub without exposing the credentials in the code.

## 📦 Docker Hub

Docker Hub repository:

https://hub.docker.com/r/kirthika2516/ci-cd-nodejs-app

Docker image:

`kirthika2516/ci-cd-nodejs-app:latest`

## ✅ Result

The CI/CD pipeline successfully automates:

Code Push → Test → Docker Build → Docker Hub Push

This project helped me understand the basics of CI/CD, GitHub Actions, Docker, Docker Hub, automated testing, and container image deployment.

## 🎓 What I Learned

- Git and GitHub
- GitHub Actions
- CI/CD concepts
- Docker and Dockerfiles
- Docker Hub
- Automated testing
- GitHub Secrets
- Docker image deployment

## 👩‍💻 Author

**Kirthika**

GitHub: https://github.com/kirthika25160
