# PSUSphere - Dockerized Environment

Beronio, Ralph Justine
Celedonio, Jan Wilhelm

This repository contains the Docker configuration files required to run **PSUSphere**, a Django-based student organization management system. It demonstrates how to containerize a Django application with SQLite and deploy it seamlessly using Docker and Docker Compose.

## 📂 Repository Structure

* `Dockerfile`: Contains the step-by-step instructions to build the PSUSphere Python image.
* `docker-compose.yml`: The main compose file used for building the image locally.
* `requirements.txt`: The isolated Python dependencies required to run the application.
* `.dockerignore`: Prevents unnecessary local files (like the local database and virtual environments) from being copied into the container.
* `for_client/`: A dedicated directory containing a separate `docker-compose.yml` for end-users to pull and run the pre-built image from Docker Hub without needing the source code.

---

## 🚀 How to Run the Application

There are two ways to run this project depending on whether you are developing the app or just deploying it.

### Option 1: For Developers (Building from Scratch)
Use this method if you want to build the Docker image locally from the `Dockerfile`.

1. Ensure Docker Desktop is running on your machine.
2. Open your terminal and navigate to the root directory of this repository.
3. Build the image and start the container in detached mode:
   ```bash
   docker compose up --build -d