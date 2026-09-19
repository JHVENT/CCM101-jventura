# Docker Deployment

## Environment

I used a KillerCoda Ubuntu Playground with Docker pre-installed.

## Step 1: Verify Docker

```bash
docker --version
docker info
```

Both commands ran without errors, which confirmed that Docker was installed and the Docker daemon was running.



## Step 2: Pull the Nginx Image

```bash
docker pull nginx
```

This downloaded the official Nginx image from Docker Hub. The image is the template that the container is created from.

## Step 3: Run the Nginx Container

```bash
docker run -d -p 8080:80 --name my-nginx nginx
```

- `-d` runs the container in the background (detached mode).
- `-p 8080:80` maps port 8080 on the host to port 80 inside the container.
- `--name my-nginx` gives the container a readable name.

I checked that it was running with:

```bash
docker ps
```

## Step 4: Test the Web Server

```bash
curl http://localhost:8080
```

The terminal returned the HTML of the "Welcome to nginx!" page, which shows the web server is running inside the container and reachable through port 8080.



## Observations

Setting up a web server on a traditional VM would mean installing an OS, installing Nginx, and configuring it. Here it took two commands and only a few seconds. Since the image already includes everything Nginx needs, I didn't have to install or configure anything by hand.
