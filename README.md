# PHP Hello World with Docker Compose

A lightweight PHP "Hello World" application containerized with Docker and orchestrated using Docker Compose.

---

## Project Structure

```text
docker-php-hello-world/
├── docker-compose.yml
├── README.md
└── src/
    └── index.php
```

---

## Prerequisites

Ensure you have the following installed and running on your local machine:
- Run `wsl --install` / `wsl.exe --install` in pwsh/cmd
- [Docker Desktop](https://docs.docker.com/desktop/setup/install/windows-install/)

---

## Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/nomedcode/docker-php-hello-world.git
cd docker-php-hello-world
```

### 2. Start the Application

Run the container in detached mode:

```bash
docker compose up -d
```

### 3. Access the Application

Open your browser and navigate to:

```text
http://localhost:8080
```

Expected output:
```text
Hello, World!
```

---

## Management Commands

| Action | Command |
|---|---|
| View container logs | `docker compose logs -f` |
| Check container status | `docker compose ps` |
| Stop and remove containers | `docker compose down` |

---

## Configuration Details

- **Web Server / Base Image:** `php:8.3-apache`
- **Host Port:** `8080`
- **Container Port:** `80`
- **Volume Mount:** `./src` mapped to `/var/www/html` for instant live-reload upon code modifications.
