# web-container-empty
A Docker Compose setup for PHP 8.4 with Apache web server.

## Features

- 🐘 PHP 8.4 with Apache
- 🔄 Auto-restart enabled
- 🌐 Port 7080 accessible via localhost
- 📁 HTML content served from `./html` directory

## Prerequisites

Before starting the container, create the external Docker network:

```bash
docker network create dockernet
```

## Usage

### Start the Container

```bash
docker compose up -d
```

### Stop the Container

```bash
docker compose down
```

## Port Configuration

The web server is accessible on **port 7080** (`127.0.0.1:7080`). This port is suitable for:
- Local development
- **VS Code port forwarding/redirection**
- Secure localhost-only access

Access the application at: `http://localhost:7080`

## Directory Structure

```
.
├── docker-compose.yml    # Docker Compose configuration
├── html/                 # Web application files (gitignored)
└── README.md            # This file
```

## Resources

- [WebDevOps Docker Images Documentation](https://webdevops.gitbook.io/dockerfile)
- [Dockerfile Reference](https://dockerfile.readthedocs.io/en/latest/)