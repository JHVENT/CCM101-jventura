# Laboratory 04 - Cloud Native Engineer

## Mission Overview

In this laboratory, I moved from theory to hands-on practice with containers. I researched how Virtual Machines and containers differ, then used a KillerCoda Ubuntu Playground with Docker to deploy an Nginx web server and manage its full lifecycle, from pulling the image to removing the container.

## Objectives

- Understand the differences between Virtual Machines and containers.
- Verify that Docker is installed and running in a cloud playground.
- Pull an official image from Docker Hub and run it as a container.
- Expose a containerized web server through port mapping.
- Manage the container lifecycle: list, stop, verify, and remove.
- Document the work clearly in a GitHub repository.

## Docker Commands Executed

### Checkpoint 3: Docker Environment

| Command | Purpose |
|---|---|
| `docker --version` | Checked that Docker is installed and showed its version. |
| `docker info` | Displayed the status and configuration of the Docker environment. |

### Checkpoint 4: Deploying Nginx

| Command | Purpose |
|---|---|
| `docker pull nginx` | Downloaded the official Nginx image from Docker Hub. |
| `docker run -d -p 8080:80 --name my-nginx nginx` | Ran Nginx in the background and mapped host port 8080 to container port 80. |
| `docker ps` | Confirmed the container was running. |
| `curl http://localhost:8080` | Sent an HTTP request and received the "Welcome to nginx!" page. |

### Checkpoint 5: Container Lifecycle

| Command | Purpose |
|---|---|
| `docker ps` | Listed the running containers. |
| `docker stop my-nginx` | Stopped the running container. |
| `docker ps -a` | Verified the container was stopped (status: Exited). |
| `docker rm my-nginx` | Removed the container completely. |

## Skills Learned

- Explaining the difference between VMs and containers in terms of architecture, boot time, resource use, and isolation.
- Using a cloud playground (KillerCoda) to practice without installing anything locally.
- Pulling images and running containers in detached mode.
- Mapping ports so a service inside a container can be reached from the host.
- Testing a web server from the terminal using `curl`.
- Managing the container lifecycle with `docker ps`, `stop`, and `rm`.
- Creating folders and files in a GitHub repository and documenting work in Markdown.

## Challenges Encountered

- **Learning GitHub:** As a beginner, I had to learn how to create folders and files on GitHub. I found out that empty folders aren't tracked by Git, so I added a placeholder file to the `screenshots` folder.
- **Understanding the tools:** At first I was unsure of the difference between KillerCoda, Docker, and Nginx. I learned that KillerCoda is the environment, Docker runs the containers, and Nginx is the web server being deployed.
- **Port mapping:** The `8080:80` format was confusing at first. It follows the pattern `host:container`.
- **Temporary sessions:** KillerCoda sessions expire, so I had to take my screenshots while the session was still active.

## Screenshots

Screenshots are stored in the `screenshots` folder:

- `docker-version.png`
- `nginx-running.png`
- `container-lifecycle.png`

