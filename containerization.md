# Containerization with Docker

## Overview
Docker allows you to run applications in isolated containers. Below are the key commands and concepts used in this project.

## Installing Docker on RedHat/Amazon Linux
```bash
sudo dnf config-manager --add-repo https://download.docker.com/linux/rhel/docker-ce.repo
sudo dnf install -y docker-ce docker-ce-cli containerd.io docker-compose-plugin
sudo systemctl start docker
sudo systemctl enable docker
```

## Key Docker Commands
```bash
docker ps                    # list running containers
docker ps -a                 # list all containers
docker compose up -d         # start all services in background
docker compose down          # stop all services
docker compose ps            # check status of services
docker logs container-name   # view container logs
```

## Running Containers
The following screenshot shows all three containers running successfully using Docker Compose:

![Containers Running](https://devop-final.s3.us-east-1.amazonaws.com/Screenshot+2026-02-25+133319.png)

## Docker Compose
Docker Compose allows you to manage multiple containers from a single file. All services, networks, and volumes are defined in docker-compose.yml and started with one command.
