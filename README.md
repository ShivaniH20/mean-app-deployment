🚀 MEAN Stack CRUD Application Deployment

MongoDB • Express • Angular • Node.js • Docker • Nginx • CI/CD (GitHub Actions)

This project is a fully containerized MEAN (MongoDB, Express, Angular, Node.js) CRUD application with automated CI/CD deployment using GitHub Actions.
The application allows users to create, read, update, delete tutorials with search capability.

🌐 Live Access
Service	URL
Frontend	http://<server-ip>/ (Nginx on port 80)
API Backend	http://<server-ip>/api/tutorials
🏗 Tech Stack
Component	Technology
Frontend	Angular 15
Backend	Node.js + Express
Database	MongoDB
Deployment	Docker + Docker Compose
Reverse Proxy	Nginx
CI/CD	GitHub Actions + Docker Hub
📁 Project Structure
crud-dd-task-mean-app/
│
├── backend/                          # Express Backend API
│   ├── Dockerfile                    # Docker build file for backend
│   ├── server.js                     # Backend entry point
│   ├── package.json
│   └── app/
│       ├── config/db.config.js       # MongoDB URL
│       ├── controllers/              # CRUD logic
│       ├── models/                   # Mongoose schemas
│       └── routes/                   # API routes
│
├── frontend/                         # Angular Frontend
│   ├── Dockerfile                    # Docker build for frontend
│   ├── package.json
│   └── src/
│       ├── app/
│       │   ├── components/
│       │   ├── services/tutorial.service.ts
│       │   └── app.module.ts
│       └── index.html
│
├── docker-compose.yml                # Multi-container deployment
├── nginx.conf                        # Reverse proxy configuration
├── .github/workflows/cicd.yml        # Automated CI/CD pipeline
├── README.md                         # Documentation
└── screenshots/                      # Required screenshots

⚙ Running Locally (Without Docker)
Backend
cd backend
npm install
node server.js


➡ Runs at: http://localhost:8080

Frontend
cd frontend
npm install
ng serve --port 8081


➡ Opens at: http://localhost:8081

🐳 Docker Deployment
sudo docker compose up -d --build


Containers Included:

Container	Port
Angular Frontend	80 (via Nginx)
Node Backend	8080
MongoDB	27017
🔥 CI/CD Automation (GitHub Actions)

Workflow tasks:

✔ Build Docker images on Git push
✔ Push images to Docker Hub
✔ SSH into VM → Pull new images & restart containers

✅ Summary

Fully containerized MEAN stack application

Deployed with Docker Compose and Nginx

CI/CD implemented using GitHub Actions

MongoDB database integrated

Screenshots included for reference


