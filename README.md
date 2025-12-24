# 🧩 WordPress with MySQL using Docker Compose

![WordPress](https://img.shields.io/badge/WordPress-Latest-blue)
![MySQL](https://img.shields.io/badge/MySQL-8.0-orange)
![Docker](https://img.shields.io/badge/Docker-Compose-blue)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

This repository provides a **simple WordPress setup using Docker Compose**, backed by a **MySQL database**.  
It is ideal for **local development, learning Docker Compose**, and quick WordPress testing without manual installation.

---

## 📁 Project Structure

```text
.
├── docker-compose.yml
└── README.md
```

---

## 🧠 What This Setup Includes

- WordPress (latest official image)
- MySQL 8.0 database
- Persistent volumes for WordPress files and database data
- Automatic internal networking via Docker Compose
- No local PHP, Apache, or MySQL installation required

---

## 🧩 Docker Compose Overview

Docker Compose defines two services:

- **wordpress** → Web application (PHP + Apache)
- **db** → MySQL database

Docker automatically creates:
- A private network
- DNS-based service communication (`db` hostname)
- Persistent storage using volumes

---

## ▶️ How to Run WordPress

### 1️⃣ Start the containers
```bash
docker compose up -d
```

---

### 2️⃣ Open WordPress in browser
```
http://localhost:8080
```

Follow the WordPress installation wizard:
- Database Host: `db`
- Database Name: `wordpress`
- Username: `wpuser`
- Password: `wppassword`

---

### 3️⃣ Stop the containers
```bash
docker compose down
```

---

### 4️⃣ Stop and REMOVE all data (⚠️ deletes DB)
```bash
docker compose down -v
```

---

## 🧠 Environment Variables Used

| Variable | Description |
|-------|------------|
| WORDPRESS_DB_HOST | MySQL hostname (service name) |
| WORDPRESS_DB_NAME | Database name |
| WORDPRESS_DB_USER | Database user |
| WORDPRESS_DB_PASSWORD | Database password |
| MYSQL_ROOT_PASSWORD | MySQL root password |

---

## 🧠 Key Concepts Demonstrated

- Multi-container Docker Compose setup
- Service-to-service communication
- Persistent volumes
- WordPress + MySQL architecture
- Local development without manual setup

---

## 📌 Requirements

- Docker Desktop
- Docker Compose (v2+)
- Windows / macOS / Linux

---

## 📄 License

This project is provided for learning and development purposes.
