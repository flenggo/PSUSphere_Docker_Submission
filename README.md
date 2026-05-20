Beronio, Ralph Justine
Celedonio, Jan Wilhelm

# PSUSphere - Docker Deployment

## 📂 Repository Structure

* `Dockerfile`: Contains the step-by-step instructions to build the PSUSphere Python image
* `docker-compose.yml`: The main compose file used for building the image locally
* `requirements.txt`: The isolated Python dependencies required to run the application
* `.dockerignore`: Prevents unnecessary local files (like the local database and virtual environments) from being copied into the container
* `for_client/`: A dedicated directory containing a separate `docker-compose.yml` for project partners to pull and run the pre-built image from Docker Hub without needing the source code

---

## 🚀 How to Run the Application (For Partners/Clients)

To test the application with a single command without building it from scratch, follow these steps

1. **Prerequisites**: Ensure Docker Desktop is installed and running on your machine
2. **Navigate to the client folder**:
   Open your terminal and navigate into the `for_client` directory of this cloned repository:
   cd for_client

Run the application:

Start the container using Docker Compose.
This will automatically pull the pre-built image (ralphjustineberonio/psusphere-app:latest) from Docker Hub:
docker compose up -d

Access PSUSphere:
Once the container is running, open your web browser and navigate to:
http://localhost:8000
