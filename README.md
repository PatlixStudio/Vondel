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