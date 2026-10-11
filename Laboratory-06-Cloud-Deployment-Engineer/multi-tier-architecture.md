# Two-Tier Architecture

## What Is a Two-Tier Architecture?

A two-tier architecture is a system with two parts that work together: the web application and the database. The web application handles what the user sees, while the database stores the information.

## The Web/Application Tier

The web/application tier is the part that users access through their browser. It displays web pages, processes requests, and communicates with the database when information needs to be saved or retrieved. In our lab, this is the **web container**.

## The Database Tier

The database tier stores the application's information, such as user accounts and other records. The data can still be accessed later even after the user closes the browser, as long as it has been saved properly. In our lab, this is the **database container**.

## Why Separate Them?

I think separating the two tiers makes the system easier to manage because each one has its own purpose. For example, the web application can be updated without necessarily changing the database. It also makes it easier to maintain each part, although both containers still need to communicate properly.

## Sources

1. Docker Docs. [What is a container?](https://docs.docker.com/get-started/docker-concepts/the-basics/what-is-a-container/)
   Date accessed: October 11, 2026.

2. Microsoft Learn. [N-tier architecture style](https://learn.microsoft.com/en-us/azure/architecture/guide/architecture-styles/n-tier)
   Date accessed: October 11, 2026.

