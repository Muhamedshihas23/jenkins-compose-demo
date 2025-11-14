#Jenkins + Docker Compose CI/CD Pipeline

This project demonstrates an automated CI/CD pipeline using Jenkins, Docker Compose, and GitHub to deploy a 3-tier application (Web + API + Database).

 Overview

Pipeline performs:

Pull latest code from GitHub

Build Docker images

Deploy multi-container app using Docker Compose

Run Web (Nginx), API (Flask), and MySQL services automatically

 Project Structure
├── Jenkinsfile
├── docker-compose.yml
├── web/
│   ├── Dockerfile
│   └── index.html
├── api/
│   ├── Dockerfile
│   └── app.py
└── db/ (MySQL 5.7)

 Docker Compose

Runs all 3 services:

web → Nginx frontend (port 8081)

api → Python Flask API (port 5000)

db → MySQL database (port 3306)

 Jenkins Pipeline

Jenkinsfile automates:

docker compose build
docker compose down
docker compose up -d


Triggered by GitHub or manual build.

 Running the Pipeline

Push code to GitHub

Jenkins pulls repository

Builds Docker images

Deploys containers

Application runs automatically

 Access the App

Frontend: http://localhost:8081

API: http://localhost:5000

 Result

✔ Fully automated CI/CD pipeline
✔ Multi-container deployment
✔ Perfect DevOps portfolio project
