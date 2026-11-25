# EazyBank Microservices

Spring Boot microservices for the EazyBank sample banking application: `configserver`, `accounts`, `loans`, and `cards`.

## Repository layout

| Path                | Purpose                                              |
|---------------------|------------------------------------------------------|
| `accounts/`         | Accounts microservice (port 8080)                    |
| `loans/`            | Loans microservice (port 8090)                       |
| `cards/`            | Cards microservice (port 9000)                       |
| `build-scripts/`    | Builds (and optionally pushes) Docker images for all services |
| `docker-compose.yml`| Runs the published images together on a bridge network |

## Running with Docker Compose

From the repository root:

```bash
docker compose up -d
docker compose down
```

## Building images

See [`build-scripts/README.md`](build-scripts/README.md) for building all service images in one command, with options for parallel builds and pushing to Docker Hub.

```bash
./build-scripts/build-images.sh -p
```

## Prerequisites

- Docker (with the daemon running)
- Maven and a JDK, for building the services locally or via the build scripts
