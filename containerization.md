# Containerization

## Common Docker Commands

- `docker ps` - List running containers
- `docker compose up -d` - Start services in background
- `docker compose down` - Stop and remove containers
- `docker compose logs <service>` - View service logs
- `docker images` - List local images
- `docker volume ls` - List volumes

## Docker Compose Structure
```yaml
services:
  app:
    image: myapp:latest
    ports:
      - "80:80"
    networks:
      - my_network

networks:
  my_network:
    driver: bridge

volumes:
  my_data:
```

## Tips
- Always pin image versions instead of using latest in production
- Use named volumes for persistent data
- Use depends_on to control startup order
- Store secrets in .env files, never hardcode them
