# RUTHWIK DOVALA (801431661)
Email ID: rdovala@charlotte.edu
# Cloud Computing for Data Analysis – Hands-On L3
ITCS 6190/8190 – Fall 2025

This repo contains a Flask + Redis app containerized with Docker and orchestrated via Docker Compose.

### 1. Install Docker Desktop (Windows)
- Downloaded and installed **Docker Desktop**.  
- Enabled **WSL 2** integration when prompted.  
- Verified installation:
  ```bash
  docker -v

### 2. PostgreSQL Setup
- Pulled PostgreSQL image:
   ```bash
   docker pull postgres
- Started PostgreSQL Container:
  ```bash
  docker run -d -p 5432:5432 --name postgres1 -e POSTGRES_PASSWORD=pass12345 postgres
- Accessed container and connected to PostgreSQL:
  ```bash
  docker exec -it postgres1 bash
  psql -d postgres -U postgres
### 3. Flask + Redis Application
- Created requirements.txt:
  ```bash
  flask
  redis
- Implemented app.py (Hello World counter using Redis).
- Wrote Dockerfile to containerize Flask.
- Defined services in compose.yaml for Flask (web) and Redis.

### 4.Build & Run Application
- 
  ```bash
  docker compose up --build

- Accessed in browser at: http://localhost:8000

- Output confirmed:
  ```bash
  Hello World! I have been seen x times
