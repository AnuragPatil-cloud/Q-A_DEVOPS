# ☁ Google Cloud Platform (GCP) Interview Questions & Answers (DevOps)

This section contains commonly asked **GCP interview questions for DevOps Engineers (Fresher – 2+ Years Experience).**

---

# 1. What is Google Cloud Platform (GCP)?

Google Cloud Platform (GCP) is a **cloud computing platform provided by Google** that offers services for computing, storage, networking, machine learning, and data analytics.

It allows organizations to **run applications and store data on Google’s infrastructure.**

---

# 2. What are the main benefits of GCP?

- Global infrastructure
- High scalability
- Pay-as-you-go pricing
- High availability
- Integration with Google services

---

# 3. What are the main categories of GCP services?

- Compute
- Storage
- Networking
- Databases
- Security
- Monitoring
- Big Data
- Machine Learning

---

# 4. What is Google Compute Engine (GCE)?

Compute Engine provides **virtual machines (VMs) that run in Google's data centers.**

Features:

- Custom machine types
- Persistent disks
- Autoscaling
- Load balancing

---

# 5. What is Google Kubernetes Engine (GKE)?

GKE is a **managed Kubernetes service in GCP** that allows you to run containerized applications.

Benefits:

- Managed Kubernetes control plane
- Automatic upgrades
- Auto scaling
- Integrated monitoring

---

# 6. What is Google Cloud Storage?

Google Cloud Storage is an **object storage service used to store files, backups, and large data.**

Features:

- High durability
- Global availability
- Lifecycle management

Storage classes:

- Standard
- Nearline
- Coldline
- Archive

---

# 7. What is Google Cloud IAM?

IAM (Identity and Access Management) is used to **control access to GCP resources.**

Components:

- Users
- Roles
- Permissions
- Service accounts

---

# 8. What is a Service Account?

A service account is a **special account used by applications or services to access GCP resources.**

Example:

A Kubernetes pod accessing a storage bucket.

---

# 9. What is a VPC in GCP?

VPC (Virtual Private Cloud) is a **virtual network used to connect GCP resources securely.**

Features:

- Subnets
- Firewall rules
- Routing
- Private IP communication

---

# 10. What are Firewall Rules in GCP?

Firewall rules control **inbound and outbound traffic** to resources in a VPC.

Example rules:

- Allow SSH (port 22)
- Allow HTTP (port 80)

---

# 11. What is Cloud Load Balancing?

Cloud Load Balancing distributes incoming traffic across multiple backend services.

Benefits:

- High availability
- Scalability
- Automatic failover

---

# 12. What is Cloud SQL?

Cloud SQL is a **managed relational database service**.

Supported databases:

- MySQL
- PostgreSQL
- SQL Server

---

# 13. What is BigQuery?

BigQuery is a **serverless data warehouse used for large-scale data analytics.**

It allows running SQL queries on massive datasets.

---

# 14. What is Cloud Functions?

Cloud Functions is a **serverless compute service** that runs code in response to events.

Example triggers:

- HTTP requests
- Cloud Storage events
- Pub/Sub messages

---

# 15. What is Cloud Run?

Cloud Run is a **fully managed service used to run containerized applications.**

It automatically scales containers based on incoming requests.

---

# 16. What is Google Cloud Monitoring?

Cloud Monitoring is used to **track performance and health of GCP resources.**

Features:

- Metrics
- Alerts
- Dashboards

---

# 17. What is Cloud Logging?

Cloud Logging collects and stores logs from GCP services and applications.

---

# 18. What is Infrastructure as Code in GCP?

Infrastructure as Code allows infrastructure to be managed using code.

Tools used with GCP:

- Terraform
- Deployment Manager

---

# 19. Real DevOps Scenario

### Problem

Application traffic increases suddenly.

### Solution

Use:

- Load Balancer
- Auto scaling
- Kubernetes (GKE)

This ensures scalability and high availability.

---

# 20. Why GCP is Important for DevOps

GCP helps DevOps teams:

- Deploy scalable infrastructure
- Run containerized applications
- Monitor systems
- Automate infrastructure

GCP integrates with:

- Kubernetes
- Docker
- Terraform
- Jenkins
- GitHub Actions
