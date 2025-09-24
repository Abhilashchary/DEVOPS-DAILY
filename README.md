DevOps Daily 🚀

DevOps Daily is a simple, single-page web application that displays a daily inspirational quote. This project is designed to showcase a complete DevOps workflow using Docker, GitHub Actions, and Render for CI/CD.

Website: https://devops-daily.onrender.com

📌 Project Overview

The goal of this project is to demonstrate a real-world DevOps pipeline. Every time a quote is updated in quotes.txt and pushed to GitHub, the pipeline automatically:

Builds a new Docker image.

Pushes the image to DockerHub.

Deploys the updated app on Render.

This makes your app instantly updated with zero manual intervention.

📁 Project Structure
DEVOPS-DAILY/
├── Dockerfile
├── index.html
├── quotes.txt
├── .github/workflows/main.yml
├── server.js
└── README.md


Dockerfile — Build instructions for Docker.

index.html — Main webpage displaying quotes.

quotes.txt — List of daily quotes.

main.yml — GitHub Actions pipeline for CI/CD.

server.js — Node.js server (optional enhancement).

🛠 Requirements

GitHub account

Docker (optional for local development)

Node.js & npm (optional for local development)

Render account

DockerHub account

🚀 Local Development

Clone the repository:

git clone https://github.com/Abhilashchary/DEVOPS-DAILY.git
cd DEVOPS-DAILY


Install dependencies (if using Node.js server):

npm install


Run the app locally:

npm start


Visit http://localhost:8080 to view.

🐳 Docker Setup

Build Docker image:

docker build -t devops-daily .


Run container:

docker run -p 8080:80 devops-daily


Visit http://localhost:8080.

⚙ CI/CD Pipeline (GitHub Actions)

The .github/workflows/main.yml file defines the pipeline:

Triggers: on push to main branch.

Steps:

Checkout code

Setup QEMU and Docker Buildx

Login to DockerHub

Build and push Docker image

Run tests

Cleanup containers

🌐 Deployment on Render

Steps:

Create a new web service.

Choose Docker environment.

Set environment variables:

DOCKERHUB_USERNAME

DOCKERHUB_TOKEN

RENDER_API_KEY

Set branch to main.

Enable auto-deploy.

Set build/start commands:

docker build -t devops-daily .
docker run -p 8080:80 devops-daily

🔐 Secrets Management

Render: Environment variables for sensitive data.

GitHub: Repository Secrets for CI/CD.

📄 License

This project is licensed under the MIT License.

Project Website: https://devops-daily.onrender.com
