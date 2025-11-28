🚀 MEAN Stack CRUD Application Deployment












This repository contains a full-stack MEAN (MongoDB, Express, Angular, Node.js) CRUD Application, fully containerized and deployed using Docker + Nginx + CI/CD automation.
Users can Create, Read, Update, Delete tutorials with search functionality.
---
📌 **Project Overview
Component	Technology
Frontend	Angular 15
Backend	Node.js + Express REST API
Database	MongoDB
Orchestration	Docker Compose
Reverse Proxy	Nginx
CI/CD Automation	GitHub Actions

✔ Node.js API for CRUD operations
✔ Angular UI for accessing backend APIs
✔ MongoDB database (container or local)
✔ Nginx reverse proxy → Application accessible on port 80
---
📂 Repository Structure
crud-dd-task-mean-app/
├── backend/                        # Express backend API
│   ├── Dockerfile                  # Backend docker image build file
│   ├── server.js                   # Entry point for backend
│   ├── package.json
│   └── app/
│       ├── config/db.config.js     # MongoDB connection settings
│       ├── controllers/            # CRUD controller logic
│       ├── models/                 # Mongoose schemas/models
│       └── routes/                 # API endpoints
│
├── frontend/                       # Angular UI application
│   ├── Dockerfile                  # Frontend docker image build file
│   ├── package.json
│   └── src/
│       ├── app/
│       │   ├── components/         # UI components
│       │   ├── services/           # API service layer
│       │   └── app.module.ts
│       └── index.html
│
├── docker-compose.yml              # Multi-container deployment
├── nginx.conf                      # Reverse proxy config
├── .github/workflows/cicd.yml      # GitHub Actions deployment workflow
├── README.md                       # Project documentation
└── screenshots/                    # Deployment proof & execution screenshots
---
🛠** Local Setup
Backend
cd backend
npm install
node server.js
---

➡ Runs at: http://localhost:8080

Frontend
cd frontend
npm install
ng serve --port 8081


➡ UI: http://localhost:8081
---
🐳 Docker Deployment
sudo docker compose up -d --build

**Service	Port
Backend	8080
Frontend (via Nginx)	80
MongoDB	27017
---
**Nginx routes:

/api → Node backend
/    → Angular frontend

⚡ **CI/CD Pipeline (GitHub Actions)
---
Automations included:

**Action	Status
Build Docker Images	✔ On every push
Push to Docker Hub	✔ Automatic
Pull & Deploy in VM	✔ Auto restart containers
---
Workflow file: .github/workflows/cicd.yml
---
✅ Summary

✔ Fully containerized MEAN stack
✔ Reverse proxy using Nginx
✔ CI/CD implemented using GitHub Actions
✔ MongoDB + Express API working
✔ Angular UI integrated with backend

