# 🐳 Docker React Deployment Practice

> A containerized full-stack React application demonstrating real-world Docker workflows — from writing Dockerfiles to orchestrating multi-container environments with Docker Compose.

---

## 📌 Overview

This project showcases the containerization and deployment of a React-based web application using Docker. The goal is to simulate a production-like deployment pipeline entirely through containers, demonstrating proficiency in Docker fundamentals, image management, and multi-service orchestration.

**Base application codebase** provided by [SoftUni](https://softuni.bg/) as part of their curriculum.  
**DevOps / Containerization work** — writing Dockerfiles, building and pushing images to Docker Hub, and authoring the `docker-compose.yml` — completed independently by me (Jeko Gyulev - author of this repository).

---

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| **React** | Frontend SPA framework |
| **Node.js** | JavaScript runtime environment |
| **Docker** | Containerization platform |
| **Docker CLI** | Image & container management via terminal |
| **Docker Compose** | Multi-container orchestration |
| **Docker Hub** | Remote image registry for publishing images |

---

## 🏗️ What I Built

### ✅ Dockerfile(s)
- Wrote a single-stage `Dockerfile` to containerize the React application for both backend and frontend services (you can find the Dockerfiles in subfolders `/backend` and `/frontend`) 
- Handled dependency installation, build steps, and serving the final app efficiently


### ✅ Docker Hub Integration
- Built Docker images locally using the Docker CLI
- Tagged images appropriately for versioning and readability
- Pushed images to a public Docker Hub repository for distribution and accessibility

### ✅ Docker Compose
- Authored a `docker-compose.yml` to define and orchestrate all services
- Configured service dependencies, port mappings, and environment variables
- Enabled single-command startup of the entire application stack (`docker compose up`)

---

## 🚀 Getting Started

### Prerequisites

Make sure you have the following installed:

- [Docker](https://www.docker.com/get-started) `v20+`
- [Docker Compose](https://docs.docker.com/compose/) `v2+`

### Run with Docker Compose

```bash
# Clone the repository
git clone https://github.com/JekoGyulev/Docker-React-Deployment-Practice.git
cd Docker-React-Deployment-Practice

# Start all services
docker compose up -d
```

The application will be available at `http://localhost:3000` (you could change it if you would like to).

### Remove containers, networks, volumes and images written in the docker-compose file

```bash
docker compose down --rmi all -v
```

---

## 🐋 Docker Hub

The built images ( `backend service` and `frontend service` of the React App) are publicly available on Docker Hub:

```bash
docker pull jeko777/backend
docker pull jeko777/frontend
```

---

## 📁 Project Structure

```
/
├── backend/                 # React backend (SoftUni base codebase) 
│   ├── logs/
│   ├── models/
|   └── app.js
|   └── Dockerfile
│   └── package.json
├── frontend/                # React frontend (SoftUni base codebase)
│   ├── public/
│   ├── src/
│   └── Dockerfile
|   └── package-lock.json
|   └── package.json        
├── docker-compose.yml       # Multi-container orchestration config
└── README.md
```

---

## 🔍 Key Docker Concepts Demonstrated

- **Image Building** — Creating optimized Docker images from a `Dockerfile`
- **Container Lifecycle** — Running, stopping, and removing containers via the Docker CLI
- **Port Mapping** — Exposing container ports to the host machine
- **Volume Mounting** — Persisting or sharing data between host and container
- **Registry Workflow** — Tagging and pushing images to Docker Hub
- **Service Orchestration** — Coordinating multiple services with Docker Compose

---

## 📜 Credits

- **Base React Application** — [SoftUni](https://softuni.bg/) — provided as a course exercise
- **Containerization & DevOps Layer** — [Jeko Gyulev](https://github.com/JekoGyulev)

---

## 📄 License

This project is intended for educational and portfolio purposes.

---

<p align="center">Made with 💙 and a lot of <code>docker</code> commands</p>
