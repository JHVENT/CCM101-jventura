# Docker Compose Guide

## 1. What Does the `services:` Block Do?

The `services:` block defines the containers that Docker Compose needs to run. In our YAML file, it contains the Nextcloud application and the database. Each service has its own settings, such as the image to use, environment variables, ports, and volumes. This makes it easier to manage both containers in one file.

## 2. How Did the Nextcloud App Container Find the Database Container?

The Nextcloud container finds the database through the `MYSQL_HOST` environment variable. This variable tells Nextcloud which hostname to use when connecting to the database. In our Docker Compose file, the value is usually the database service name, such as `db`. Docker Compose allows containers on the same network to communicate using their service names, so we do not need to use the database container's IP address directly.

## 3. Difference Between `docker run` and `docker-compose up -d`

The `docker run` command is used to create and start an individual container with the options specified in the command. If an application needs multiple containers, we may need to run separate commands and configure their connections.

On the other hand, `docker-compose up -d` starts the services defined in the Docker Compose YAML file in the background. It can start both the Nextcloud application and the database together using the settings in that file. The `-d` option means detached mode, so the containers keep running without occupying the terminal.

I think Docker Compose is more convenient for applications with multiple containers because the configuration is stored in one file instead of requiring several long commands.

