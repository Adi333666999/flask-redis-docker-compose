# Flask + Redis with Docker Compose

A hands-on Docker project demonstrating how to containerize a Flask application and connect it to Redis using Docker Compose.

This project focuses on Docker fundamentals, container networking, image building, Docker Compose, Redis communication, and troubleshooting.

---

## Architecture

```text
                    Docker Compose
                         |
              -------------------------
              |                       |
              v                       v
        Flask Web Container      Redis Container
        flask-redis-compose      redis:alpine
              |                       |
              |---- Docker Network ---|
                       |
                  redis:6379
              |
        Host Port 5000
              |
              v
        http://localhost:5000