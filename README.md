#🚀 MEAN Stack CRUD Application Deployment & Automation Project
--
[![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white)]()
[![Node.js](https://img.shields.io/badge/Node.js-339933?logo=node.js&logoColor=white)]()
[![Angular](https://img.shields.io/badge/Angular-DD0031?logo=angular&logoColor=white)]()
[![MongoDB](https://img.shields.io/badge/MongoDB-47A248?logo=mongodb&logoColor=white)]()
[![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?logo=github-actions&logoColor=white)]()


This repository contains a full-stack MEAN (MongoDB, Express, Angular, Node.js) CRUD application, fully containerized and deployed with Docker, Nginx reverse proxy, and CI/CD automation. Users can create, read, update, and delete tutorials, with search functionality by title.
--
📌 **Problem Statement 1:** MEAN Application Containerization & Deployment
Objective: Containerize the MEAN stack application and deploy it using Docker Compose with secure communication via Nginx reverse proxy.

✔ Key Deliverables

Dockerfiles → Containerized backend (Node.js + Express) and frontend (Angular 15)
Docker Compose → Multi-container setup including MongoDB and Nginx
Service Exposure → Frontend accessible on port 80, backend APIs routed via Nginx
GitHub Actions Workflow → Automates image build, push to registry, and deployment on VM
Nginx Reverse Proxy → Handles routing and serves static frontend files

📌 **Problem Statement 2:** Application Features & Automation
Objective: Implement CRUD operations, search functionality, and basic automation for the application.

✔ Key Deliverables

Backend APIs → RESTful endpoints for tutorials (create, read, update, delete)
Frontend UI → Angular components for adding, listing, and editing tutorials
Search Functionality → Filter tutorials by title
Database Integration → MongoDB for data persistence
CI/CD Pipeline → Automated build and deployment on push to GitHub

📌 **Problem Statement 3:** Security & Best Practices
#Objective: Ensure secure deployment and configuration for the MEAN stack application.

✔  Key Deliverables

Environment Variables → Secure MongoDB credentials and API endpoints
Nginx Configuration → Reverse proxy for API routing and static file serving
Docker Security → Non-root user in containers, minimal base images
Screenshots → Documentation of running application, Docker Compose, and CI/CD workflow
--
##🛠️ How to Run
Clone this repository:

bash

Copy code
git clone https://github.com/your-username/crud-dd-task-mean-app.git
cd crud-dd-task-mean-app
Local Development
Backend (Node.js + Express):

bash

Copy code
cd backend
npm install
node server.js
Backend runs on port 8080 by default.

Frontend (Angular 15):

bash

Copy code
cd frontend
npm install
ng serve --port 8081
Frontend accessible at: http://localhost:8081
--
**Docker Deployment**
Build and start containers using Docker Compose:

bash

Copy code
sudo docker compose up -d --build
Containers included:

Backend: Node.js + Express
Frontend: Angular 15
MongoDB: Official MongoDB image
Nginx: Serves frontend on port 80 and routes API requests to backend.

📂 Repository Structure 

crud-dd-task-mean-app/
├── backend/                              # Node.js + Express backend API
│   ├── Dockerfile                         # Backend image build file
│   ├── package.json                       # Backend dependencies & scripts
│   ├── server.js                          # Backend entry point
│   └── app/
│       ├── config/
│       │   └── db.config.js               # MongoDB configuration setup
│       ├── controllers/
│       │   └── tutorial.controller.js     # CRUD logic for tutorials
│       ├── models/
│       │   ├── index.js                   # Mongoose model initialization
│       │   └── tutorial.model.js          # Tutorial schema/model
│       └── routes/
│           └── tutorial.routes.js         # REST API routing
│
├── frontend/                              # Angular 15 frontend application
│   ├── Dockerfile                         # Frontend image build file
│   ├── package.json                       # Angular dependencies & scripts
│   └── src/
│       ├── app/
│       │   ├── components/                # UI components
│       │   │   ├── add-tutorial/
│       │   │   ├── tutorial-details/
│       │   │   └── tutorials-list/
│       │   ├── services/
│       │   │   └── tutorial.service.ts    # Service for backend API calls
│       │   └── app.module.ts              # Main Angular module
│       └── index.html                     # Angular entry point
│
├── docker-compose.yml                     # Multi-container deployment setup
├── README.md                              # Project documentation
└── screenshots/                           # CI/CD + UI proof screenshots


✅ Summary
Fully containerized MEAN stack application with CRUD operations and search
Deployed using Docker Compose and Nginx reverse proxy
CI/CD pipeline implemented with GitHub Actions for automated builds and deployments
MongoDB integrated for data persistence
Screenshots included for reference and verification

