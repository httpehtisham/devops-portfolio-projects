# Production-Grade 3-Tier Web Architecture

## Overview
This project demonstrates a fully containerized 3-tier application architecture using Docker Compose. It features a frontend Nginx reverse proxy, a Python/Flask backend API, and a PostgreSQL database.

## Max-Level DevOps Features Implemented
* **Network Isolation:** The database sits on a secure internal backend network (`internal: true`) and cannot be accessed from the internet.
* **Reverse Proxy:** Nginx routes web traffic and proxies `/api/` requests to the backend securely.
* **Container Health Checks:** The backend API waits for a `service_healthy` signal from the database before booting.
* **Storage Persistence:** Named volumes are utilized to ensure PostgreSQL database state survives container restarts.
* **Security & Optimization:** Uses lightweight Alpine Linux base images and a secure `.env` file for credential management.

## How to Run
1. Clone the repository.
2. Ensure Docker and Docker Compose are installed.
3. Run `docker compose up -d --build` in this directory.
4. Access the application at `http://localhost`.
