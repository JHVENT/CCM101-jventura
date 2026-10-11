# Docker Compose Mission Reflection

## 1. Docker Compose vs. Docker Run

I think Docker Compose is easier to use because I can start multiple containers using just one command. In this mission, `docker-compose up -d` started the Nextcloud application and database using the settings in my YAML file. Unlike `docker run`, which usually requires a separate command for each container, Docker Compose keeps the configuration in one file that I can reuse.

## 2. YAML Indentation

I learned that proper indentation is important when writing a YAML file because it shows which settings belong to each section. If the indentation is incorrect, Docker Compose may not understand the configuration and can return an error. This taught me to check the spaces and arrangement of my code carefully. I also realized that even a small formatting mistake can prevent the containers from starting properly.

## 3. Environment Variables

Environment variables allow the containers to use the settings they need without changing the application images. In my YAML file, `MYSQL_PASSWORD`, `MYSQL_DATABASE`, `MYSQL_USER`, and `MYSQL_HOST` help configure the database connection and credentials. I also noticed that passwords written directly in the file can be seen by anyone who has access to it. For real projects, sensitive information should be protected, especially when sharing files on GitHub.

## 4. My Experience

During this mission, I found Docker Compose useful because it made running Nextcloud and its database more organized. Instead of configuring each container separately, I could define their settings in one file. Opening Nextcloud through port 8080 also helped me understand how the application could be accessed through a browser. Although setting up containers requires careful configuration, I think the process becomes easier with practice.

## 5. Comparing Mission 1 and This Mission

In Mission 1, I was still learning the basic concepts of Docker and how containers work. Now, I understand better how multiple containers can work together as one application. I also learned that troubleshooting is part of the process, especially when a command is unavailable or an image fails to download. These experiences helped me become more comfortable with Docker and understand the importance of checking errors instead of giving up immediately.



