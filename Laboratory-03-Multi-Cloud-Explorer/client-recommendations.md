# CloudNova Technologies — Client Cloud Platform Recommendations

## Client A – Startup Company
**Recommended Platform: Amazon Web Services (AWS)**

AWS is well suited to a startup with a limited budget but expectations of rapid growth. It offers a free tier and flexible pay-as-you-go pricing, so the company only pays for what it uses in the early stages while keeping costs low. As the app scales, AWS's mature auto-scaling and serverless tools let infrastructure grow smoothly without a costly upfront redesign. Its huge ecosystem of tutorials, startup credit programs (like AWS Activate), and third-party integrations also make it easier for a small team to build quickly without deep in-house cloud expertise.

**Services the client could use:**
1. **AWS Lambda** — serverless compute to run the app's backend logic without managing servers, keeping costs low at low traffic.
2. **Amazon S3** — affordable, scalable storage for app assets, user uploads, and backups.
3. **Amazon DynamoDB** — a managed NoSQL database that scales automatically as the user base grows.

## Client B – University
**Recommended Platform: Microsoft Azure**

Since the university already relies on Windows Server, Microsoft 365, and Active Directory, Azure is the natural fit because it integrates directly with these existing systems. Migrating to Azure lets the university extend its current Active Directory identities into the cloud (via Azure AD/Entra ID) rather than rebuilding identity management from scratch. Azure's hybrid cloud tools also allow the university to migrate services gradually, keeping some systems on-premises while others move to the cloud. This reduces both the technical risk and cost of a full migration.

**Services the client could use:**
1. **Azure Active Directory (Entra ID)** — extends the university's existing identity and access management into the cloud.
2. **Azure Virtual Machines** — to migrate existing Windows Server-based applications with minimal changes.
3. **Azure Files / Blob Storage** — cloud file storage that integrates with existing Windows-based workflows.

## Client C – AI Research Company
**Recommended Platform: Google Cloud Platform (GCP)**

GCP is the strongest choice for an AI/ML research company needing high-performance computing. It offers some of the most advanced machine learning infrastructure available, including custom AI accelerators (TPUs) that are exclusive to Google Cloud and optimized for training large models. GCP's tools are also deeply integrated with popular open-source ML frameworks like TensorFlow, which Google itself developed. Additionally, GCP's strength in large-scale data analytics (via BigQuery) supports the massive datasets typically required for AI research.

**Services the client could use:**
1. **Vertex AI** — a unified platform for building, training, and deploying machine learning models.
2. **Compute Engine with TPUs/GPUs** — high-performance computing instances optimized for AI model training.
3. **BigQuery** — a serverless data warehouse for processing and analyzing the large datasets used in research.

## Client D – Global E-Commerce Company
**Recommended Platform: Amazon Web Services (AWS)**

AWS is the best fit for a multinational e-commerce company because it has the largest global footprint of regions and Availability Zones among the major providers, allowing the company to keep infrastructure close to customers worldwide for low latency. AWS's auto-scaling and load-balancing services are mature and battle-tested at massive scale, having powered Amazon's own retail operations for years. Its wide range of services also means the company can handle everything from web hosting to inventory databases to fraud detection within a single ecosystem. This combination of global reach, reliability, and scalability makes AWS well suited for high-availability, worldwide e-commerce traffic.

**Services the client could use:**
1. **Amazon EC2 with Auto Scaling** — automatically adjusts server capacity based on traffic demand during sales events or peak periods.
2. **Amazon CloudFront** — a global content delivery network (CDN) that speeds up content delivery to customers worldwide.
3. **Amazon RDS (with Multi-AZ deployment)** — a managed, highly available relational database for order and inventory data.

