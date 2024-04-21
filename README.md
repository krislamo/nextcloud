# Nextcloud Deployment Repository

This repository contains configurations for deploying Nextcloud using Docker.
Nextcloud is an open-source platform that provides secure data storage,
sharing, and access across devices. It is a self-hosted alternative to cloud
storage services and offers features like file sharing, calendar and contact
management, and collaborative editing tools.

## Docker Configuration

- `IMAGE`: Specifies the Docker image for Nextcloud (default: `nextcloud`).
- `VERSION`: Specifies the tag of the Docker image (default: `latest`).
- `NAME`: Sets the name of the Docker container (default: `nextcloud`).

## Nextcloud Configuration

- `PHP_MEMORY_LIMIT`: Sets the memory limit for PHP processes (default: `1024M`).

## Traefik Configuration

- `ROUTER`: Defines the router name for Traefik to use (default: `nextcloud`).
- `DOMAIN`: Specifies the domain for accessing Nextcloud (default: `cloud.local.krislamo.org`).
- `ENTRYPOINT`: Configures the Traefik entrypoint (default: `web`).
- `ENABLE_TLS`: Toggles TLS encryption (default: `false`).
- `CONTAINER_PORT`: Specifies the HTTP port used for Traefik (default: `80`).
- `MIDDLEWARES`: Lists the middlewares applied to the Nextcloud service (default: `nextcloud-webdav`).

## Network Configuration
- `NETWORK`: Designates the Docker network to be used (default: `traefik`).

## Volume Configuration
- `DATA`: Required. Specifies the path for persistent data storage for Nextcloud.

## License
This project is released under the 0BSD license, which allows for unrestricted
use, modification, and distribution.
