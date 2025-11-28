MEAN Stack CRUD Application Deployment

This repository contains a full-stack MEAN (MongoDB, Express, Angular, Node.js) CRUD application, fully containerized and deployed with Docker, Nginx, and CI/CD automation. Users can create, read, update, and delete tutorials, with search functionality by title.

📌 Project Overview

Backend: Node.js + Express REST APIs connected to MongoDB

Frontend: Angular 15 application consuming backend APIs

Database: MongoDB (Docker container or local installation)

Deployment: Docker Compose + Nginx reverse proxy

CI/CD: GitHub Actions for automated build, push, and deployment

📂 Repository Structure
crud-dd-task-mean-app/
├── backend/                    # Node.js + Express backend
│   ├── Dockerfile              # Dockerfile for backend
│   ├── package.json            # Dependencies & scripts
│   ├── server.js               # Entry point for backend
│   └── app/
│       ├── config/
│       │   └── db.config.js    # MongoDB configuration
│       ├── controllers/
│       │   └── tutorial.controller.js
│       ├── models/
│       │   ├── index.js
│       │   └── tutorial.model.js
│       └── routes/
│           └── tutorial.routes.js
├── frontend/                   # Angular frontend
│   ├── Dockerfile              # Dockerfile for frontend
│   ├── package.json            # Dependencies & scripts
│   └── src/
│       ├── app/
│       │   ├── components/
│       │   │   ├── add-tutorial/
│       │   │   ├── tutorial-details/
│       │   │   └── tutorials-list/
│       │   ├── services/
│       │   │   └── tutorial.service.ts
│       │   └── app.module.ts
│       └── index.html
├── docker-compose.yml          # Multi-container deployment
├── README.md                   # Project documentation
└── screenshots/                # Screenshots for deployment and CI/CD

🛠️ Setup Instructions
Backend (Node.js + Express)
cd backend
npm install


Update MongoDB credentials in app/config/db.config.js if required

Run the backend server:

node server.js


Backend runs on port 8080 by default.

Frontend (Angular 15)
cd frontend
npm install
ng serve --port 8081


Frontend is accessible at:

http://localhost:8081


Modify tutorial.service.ts to adjust backend API endpoints if needed

Docker Deployment

Build and start containers using Docker Compose:

sudo docker compose up -d --build


Containers included:

Backend: Node.js + Express

Frontend: Angular 15

MongoDB: Official MongoDB image

Nginx serves the frontend on port 80 and routes API requests to backend.

CI/CD Pipeline (GitHub Actions)

Automatically builds Docker images on GitHub push

Pushes images to Docker Hub

Pulls latest images on VM and restarts containers

🖼 Screenshots

Include in screenshots/ folder:

Backend running

Frontend running

Docker Compose up

Nginx reverse proxy

CI/CD workflow execution

✅ Summary

Fully containerized MEAN stack application

Deployed with Docker Compose and Nginx

CI/CD implemented using GitHub Actions

MongoDB database integrated

Screenshots included for reference

