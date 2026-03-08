# 🔁 Jenkins Interview Questions & Answers (DevOps)

This section contains commonly asked **Jenkins interview questions for DevOps Engineers (Fresher – 2+ Years Experience).**

---

# 1. What is Jenkins?

Jenkins is an **open-source automation server** used to implement **Continuous Integration (CI) and Continuous Deployment (CD)**.

It automates tasks like:

- Building applications
- Running tests
- Deploying applications

---

# 2. What is CI/CD?

CI/CD stands for:

Continuous Integration (CI)  
Developers frequently merge code into a shared repository and automated builds/tests run.

Continuous Delivery / Deployment (CD)  
Automatically deploy applications to staging or production environments.

---

# 3. What are the main features of Jenkins?

- Open source
- Easy integration with DevOps tools
- Large plugin ecosystem
- Supports distributed builds
- Automates CI/CD pipelines

---

# 4. What is a Jenkins Pipeline?

A Jenkins Pipeline is a **set of automated steps used to build, test, and deploy applications**.

Pipelines are defined using **Jenkinsfile**.

---

# 5. What is a Jenkinsfile?

A Jenkinsfile is a **text file that defines the CI/CD pipeline using code**.

Example:

```groovy
pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building application'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application'
            }
        }
    }
}
```

---

# 6. What are Jenkins Jobs?

A Jenkins job is a **task or process configured in Jenkins to run automatically**.

Types of jobs:

- Freestyle job
- Pipeline job
- Multibranch pipeline
- Maven job

---

# 7. What is a Freestyle Project?

Freestyle project is the **simplest Jenkins job used to run basic build tasks**.

Example tasks:

- Pull code from Git
- Build project
- Run scripts

---

# 8. What are Jenkins Nodes?

Nodes are **machines that execute Jenkins jobs**.

Types:

Master Node  
Controls Jenkins and schedules jobs.

Agent Node  
Runs build jobs assigned by the master.

---

# 9. What is Jenkins Master?

The Jenkins master is responsible for:

- Scheduling jobs
- Managing agents
- Monitoring builds
- Hosting the Jenkins UI

---

# 10. What are Jenkins Agents?

Agents are machines connected to Jenkins that **execute build jobs**.

This helps distribute workload across multiple machines.

---

# 11. What are Jenkins Plugins?

Plugins extend Jenkins functionality.

Examples:

- Git Plugin
- Docker Plugin
- Kubernetes Plugin
- Pipeline Plugin
- Blue Ocean

---

# 12. Important Jenkins Plugins for DevOps

- Git Plugin
- Pipeline Plugin
- Docker Plugin
- Kubernetes Plugin
- SonarQube Plugin
- AWS Plugin

---

# 13. What is Blue Ocean in Jenkins?

Blue Ocean is a **modern UI for Jenkins pipelines** that makes pipelines easier to visualize and manage.

---

# 14. What is Jenkins Pipeline as Code?

Pipeline as Code means **defining CI/CD pipelines using code instead of manual configuration**.

This is done using **Jenkinsfile**.

Benefits:

- Version control
- Reusable pipelines
- Automated builds

---

# 15. What is the difference between Declarative and Scripted Pipeline?

Declarative Pipeline  
- Simpler syntax  
- Easier to write  

Scripted Pipeline  
- More flexible  
- Uses Groovy scripting

---

# 16. What is Jenkins Build Trigger?

Triggers automatically start Jenkins jobs.

Examples:

- Git commit trigger
- Scheduled build
- Webhook trigger

---

# 17. What is Webhook in Jenkins?

Webhook automatically **triggers a Jenkins build when code is pushed to GitHub or GitLab**.

Example flow:

Developer pushes code → GitHub webhook → Jenkins pipeline runs.

---

# 18. What are Jenkins Stages?

Stages divide the pipeline into logical sections.

Example stages:

- Build
- Test
- Security Scan
- Deploy

---

# 19. Real DevOps CI/CD Pipeline Example

Typical pipeline:

1. Developer pushes code to Git
2. Jenkins triggers build
3. Run unit tests
4. Build Docker image
5. Push image to Docker registry
6. Deploy to Kubernetes

---

# 20. Example Jenkins CI/CD Flow

```
Git → Jenkins → Build → Test → Docker Build → Push Image → Deploy Kubernetes
```

---

# 21. Important Jenkins Commands

Restart Jenkins service:

```
systemctl restart jenkins
```

Check Jenkins status:

```
systemctl status jenkins
```

---

# 22. Jenkins Default Port

Jenkins runs by default on:

```
8080
```

Example access:

```
http://server-ip:8080
```

---

# 23. Where is Jenkins home directory?

Default location:

```
/var/lib/jenkins
```

It stores:

- Jobs
- Plugins
- Logs
- Configuration

---

# 24. Real DevOps Troubleshooting Scenario

### Problem

Jenkins build failed.

### Solution

Check build logs in Jenkins console output.

Possible issues:

- Dependency failure
- Git authentication issue
- Docker build failure

---

# 25. Why Jenkins is Important for DevOps

Jenkins helps DevOps teams:

- Automate builds
- Run automated tests
- Deploy applications
- Integrate multiple tools

Jenkins integrates with:

- Git
- Docker
- Kubernetes
- Terraform
- AWS
- SonarQube
