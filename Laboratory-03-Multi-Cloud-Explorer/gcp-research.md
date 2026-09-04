# Google Cloud Platform (GCP)

## Brief Overview
Google Cloud Platform (GCP) is Google's suite of cloud computing services, built on the same infrastructure Google uses internally for products like Search and YouTube. Launched publicly in 2008 (starting with App Engine), GCP is known for strengths in data analytics, machine learning/AI, Kubernetes and container orchestration, and its global private fiber network.

## Global Infrastructure
GCP infrastructure is divided into **Regions** (independent geographic areas) and **Zones** (isolated locations within a region). As of 2026, GCP operates roughly **40+ regions** and around **120+ zones** worldwide, connected by Google's own extensive private fiber-optic network and undersea cables rather than relying solely on the public internet, which helps reduce latency between regions.

## Cloud Management Console
The **Google Cloud Console** is the web-based interface for managing GCP resources, offering project-based organization, IAM (Identity and Access Management) for permissions, Billing and Cost Management dashboards, and Cloud Shell for browser-based command-line access. GCP also provides the `gcloud` CLI, client SDKs, and Terraform/Deployment Manager support for infrastructure-as-code.

## Four (4) Core Services
1. **Compute Engine** — customizable virtual machine instances for general-purpose computing.
2. **Cloud Storage** — scalable, durable object storage for unstructured data.
3. **BigQuery** — serverless, highly scalable data warehouse for large-scale analytics using SQL.
4. **Google Kubernetes Engine (GKE)** — managed Kubernetes service for deploying and orchestrating containerized applications.

## Three (3) Advantages
1. **Leading data analytics and AI/ML tools** — services like BigQuery, Vertex AI, and TensorFlow integration give GCP an edge for data-driven and AI workloads.
2. **Strong container and Kubernetes support** — GCP originated Kubernetes internally, making GKE one of the most mature managed Kubernetes offerings available.
3. **High-performance private global network** — Google's own fiber backbone connects regions, often improving latency and throughput between services compared to routing over the public internet.

## Typical Enterprise Use Cases
- Big data processing and analytics pipelines (e.g., using BigQuery, Dataflow, Dataproc).
- Machine learning model development and deployment (e.g., Vertex AI).
- Containerized microservices architectures managed with GKE.
- Media, gaming, and content delivery workloads benefiting from Google's global network.
- Data warehousing and business intelligence for enterprises needing large-scale, real-time analytics.

