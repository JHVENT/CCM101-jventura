## Laboratory 2: Build the Cloud Infrastructure Blueprint

Mission Overview
This lab simulates the planning phase of a cloud deployment for a fictional company, CloudNova Technologies. As a newly onboarded cloud engineer, the task was to investigate the components of cloud infrastructure, understand how compute, storage, networking, and identity services work together, and document the findings as technical documentation for a client, using a Linux server running in the KillerCoda environment.

Objectives
- Explain the major components of cloud infrastructure
- Investigate the hardware and software resources available in a Linux environment
- Differentiate compute, storage, networking, and identity resources
- Interpret the relationship between cloud infrastructure components
- Create professional technical documentation using Markdown
- Continue building a structured GitHub Cloud Computing Portfolio

Cloud Infrastructure Components
Full breakdown available in cloud-components.md. In summary:
- Compute: the CPU and RAM that run applications and services
- Storage: where data persists, including the OS, files, and logs
- Networking: what connects the server to users and other systems
- Operating System: the software layer that manages hardware and runs everything else

Tools Used
- KillerCoda Playground (Ubuntu 24.04 environment)
- Linux terminal and command-line tools
- GitHub (version control and portfolio hosting)
- Mermaid.js (cloud architecture diagram)
- Markdown (documentation formatting)

Linux Commands Executed
- cat /etc/os-release — identified the operating system
- uname -r — identified the kernel version
- lscpu — identified the CPU model and number of cores
- free -h — identified total RAM
- df -h — identified disk capacity and mounted filesystems
- hostname — identified the server hostname
- hostname -I — identified the server's IP address

Skills Learned
- Investigating a Linux server's hardware and software specs from the command line
- Mapping raw system information to cloud infrastructure concepts
- Structuring a professional GitHub repository with folders, files, and meaningful commits
- Writing clear technical documentation in Markdown
- Comparing equivalent services across AWS, Azure, and Google Cloud Platform
- Creating a cloud architecture diagram using Mermaid.js

Challenges Encountered
The main challenge was getting comfortable with GitHub's file and folder system, especially creating nested folders correctly through the web interface rather than a local Git setup. A few files were initially created as empty placeholders instead of proper folders, which required deleting and recreating them with the correct path format. Understanding how to translate raw terminal command output into meaningful documentation also took some trial and error.
