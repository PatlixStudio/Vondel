# Vondel - Development Environment

This repository contains the Vondel full-stack project:

- **Backend:** NestJS (submodule)
- **Frontend:** Angular + Ionic (submodule)
- **Database:** PostgreSQL
- **Dev Environment:** Docker + Docker Compose

This setup allows developers to **run and develop the project fully in Docker** with live hot-reload.

---

## 1. Requirements

- Git (to clone submodules)
- Docker (latest version)
- Docker Compose
- Node.js (for local commands if needed)
- Optional: VS Code / IDE

---

## 2. Clone the repository with submodules

```bash
git clone --recurse-submodules https://github.com/PatlixStudio/Vondel.git
cd vondel
```

If you already cloned without --recurse-submodules

```bash
git submodule update --init --recursive
```

## 3. Run the development environment
```bash
export MY_UID=$(id -u)
export MY_GID=$(id -g)
docker compose up --build
```

## 4. Development workflow

#### Backend (NestJS)

Edit files in vondel-backend/src/

Hot-reload is automatic

API available at http://localhost:3000

#### Frontend (Angular/Ionic)

Edit files in vondel-frontend/src/

Hot-reload is automatic

UI available at http://localhost:8100

#### Database (PostgreSQL)

User: dev

Password: devpassword

Database: vondel

## 5. Useful Docker commands

Start containers (build if needed):

docker compose up --build


Start in background:

docker compose up -d


Stop containers:

docker compose down


View logs:

docker compose logs -f frontend
docker compose logs -f backend


List all containers (running and stopped):

docker ps -a

## 6. Notes

Submodules must be updated if backend or frontend repos change:

git submodule update --remote

## 7. Fork the repository

Create a branch: git checkout -b feature/your-feature

Make changes (backend/frontend in submodules)

Push to your branch

Open a pull request