Cloud Native CI/CD Platform

This repository contains a Spring Boot application with an automated CI pipeline implemented using GitHub Actions.

The purpose of this project is to demonstrate how modern application delivery is automated — from source code changes to building and publishing container images.

🏗️ CI Pipeline Architecture
Developer
    |
    v
GitHub Repository
    |
    v
GitHub Actions
    |
    +----------------+
    |                |
    v                v
 Maven Build     Docker Build
                     |
                     v
             Docker Image
                     |
                     v
              Docker Hub
🛠️ Technologies Used
Technology	    Purpose
Java            Spring Boot	Backend application
Maven	          Application build and dependency management
GitHub Actions	Continuous Integration automation
Docker	        Application containerization
Docker Hub	     Container image registry

⚙️ CI Workflow Implementation

The CI pipeline automatically runs whenever changes are pushed to the repository.

Workflow Steps:
1. Source Code Checkout
GitHub Actions retrieves the latest application source code.

2. Application Build
The Spring Boot application is built using Maven.

3. Docker Image Creation
A Docker image is created using the application Dockerfile.

4. Image Publishing
The generated Docker image is pushed to Docker Hub for deployment.

📂 Repository Structure
cloud-native-cicd-platform

│
├── src/
│   └── Spring Boot Application Code
│
├── Dockerfile
│
├── pom.xml
│
└── .github/
    └── workflows/
        └── build-and-push.yml
        
🐳 Containerization Flow
Spring Boot Application
          |
          v
       Dockerfile
          |
          v
    Docker Image Build
          |
          v
    Docker Hub Registry
