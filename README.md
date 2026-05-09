# Go Home Automation API & PWA

A lightweight, high-performance **Home Automation API** and **Progressive Web App (PWA)** built with Go. This project serves as a centralized hub for managing smart home devices, designed with a mobile-first approach and a "SQL-first" philosophy.

## 🚀 Overview

The **rdev-go-home-app** provides a robust backend architecture for controlling home environments. It is designed to be client-agnostic, serving both a built-in **PWA** for browser-based control and a **JSON API** for native mobile integration.

### Core Features

- **Device Management:** CRUD operations for lights, switches, and sensors.
- **State Persistence:** Real-time state tracking using **PostgreSQL** and **Bun ORM**.
- **Multi-Client Support:** Dedicated endpoints for Mobile (JSON) and Web (HTML/PWA).
- **Architecture:** Clean, tiered structure (`internal/` pattern) for scalability and testability.
- **Security:** Role-Based Access Control (RBAC) to manage user permissions.

## 🛠 Tech Stack

| Layer                | Technology                                    |
| -------------------- | --------------------------------------------- |
| **Language**         | Go (Golang)                                   |
| **Database**         | PostgreSQL                                    |
| **ORM**              | [Bun](https://bun.uptrace.dev/)               |
| **Caching**          | Redis                                         |
| **Containerization** | Docker                                        |
| **Web Framework**    | React.js                                      |

## 🛠 Getting Started

### Prerequisites

- Go 1.26+
- Docker & Docker Compose
- Make (optional, but recommended)

### Local Development (Docker)

The environment is configured to bridge the containerized API with your local database via `host-gateway`.

1. **Clone the repository:**
```bash
git clone https://github.com/XaiPhyr/rdev-go-api.git
cd rdev-go-api
```

2. **Spin up the environment:**
```bash
docker compose up -d --build
```
The API will be accessible at `http://localhost:8200/api/v1`.


## 📂 Folder Structure
```
.
├── api/                # Go Backend Service
│   ├── cmd/            # Entry points
│   ├── internal/       # Private application code
│   │   ├── config/     # Configuration & Env
│   │   ├── data/       # Models & Bun ORM logic
│   │   ├── dto/        # Data Transfer Objects
│   │   ├── server/     # Gin Engine & Routes
│   │   └── service/    # Business Logic
├── pwa/                # PWA / Frontend Assets
├── templates/          # HTML Templates for Go-Gin
├── docker-compose.yml  # Local Development Environment
└── README.md
```
