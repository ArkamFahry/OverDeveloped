---
id: 362hlmvangnt9zu9esmnll9
title: Docker_compose
desc: ''
updated: 1673424673577
created: 1673423404656
isDir: false
enableToc: false
tags:
  - docker
  - containers
title_imported: Docker Compose
---

**Docker compose** is used to run multiple docker containers at once

## Networking

By default Docker-Compose will create a new network for the given compose file. You can change the behavior by defining custom networks in your compose file.

### Create and assign custom network

*Example:*

```yaml
networks:
  custom-network:

services:
  app:
    networks:
      - custom-network
```

### Use existing networks

If you want to use an existing Docker network for your compose files, you can add the `external: true` parameter in your compose file
*Example:*

```yaml
networks:
  existing-network:
    external: true
```

## Volumes

Volumes allow Docker containers to use persistent storage. In a compose file, you can create and map volumes like this:

```yaml
volumes:
  my-volume:

services:
  app:
    volumes:
      - my-volume:/path-in-container
```

These volumes are stored in `/var/lib/docker/volumes`.

## Commands

COMMAND | DESCRIPTION
---|---
`docker compose up -d` | Start a new container stack
`docker compose down` | Stops the container stack
`docker compose down --remove-orphans` | Stops the container stack and Remove containers for services not defined in the Compose file
