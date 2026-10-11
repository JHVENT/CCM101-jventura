# Laboratory 06 – Cloud Deployment Engineer

## Mission Overview
As a cloud deployment engineer at CloudNova Technologies, I deployed a private cloud storage system for a university client using Docker Compose. The stack has two tiers, a MariaDB database container and a Nextcloud web container, and both were started with a single command from a `docker-compose.yml` file.

## Objectives
- Explain what a multi-tier application architecture is.
- Understand the purpose and structure of a `docker-compose.yml` file.
- Create a configuration file using the `nano` text editor.
- Deploy and tear down a multi-container application with Docker Compose.
- Document the deployment in Markdown and keep my GitHub portfolio updated.

## Commands Executed
```bash
mkdir nextcloud-deployment
cd nextcloud-deployment
nano docker-compose.yml
cat docker-compose.yml
docker-compose up -d
docker-compose ps
docker-compose down
```

Note: `docker compose` (with a space) returned "unknown command" in this playground, so I used the hyphenated `docker-compose` instead.

## Skills Learned
- Writing a multi-service `docker-compose.yml` file with correct YAML indentation.
- Deploying and removing a whole stack with `docker-compose up -d` and `docker-compose down`.
- Checking running containers with `docker-compose ps`.
- Reaching a containerized web app through a mapped port (8080).
- Documenting infrastructure work in Markdown.

## AI Use Disclosure
AI was used for step-by-step guidance on the lab and to check my drafts. The architecture research, the Compose guide and the reflection are my own work.
