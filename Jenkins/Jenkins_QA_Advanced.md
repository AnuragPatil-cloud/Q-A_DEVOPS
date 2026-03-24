# ⚙ Jenkins Interview Questions & Answers (2+ Years DevOps)

This section contains **in-depth Jenkins interview Q&A with real DevOps usage**.

---

# 1. What is Jenkins?

## Answer
Jenkins is an **open-source automation server used to build, test, and deploy applications (CI/CD)**.

## Real DevOps Usage
👉 Used to:
- automate build and deployment
- integrate code changes
- reduce manual effort

---

# 2. What is CI/CD?

## Answer
CI (Continuous Integration) → Automatically build & test code  
CD (Continuous Deployment/Delivery) → Automatically deploy application  

## Real DevOps Usage
👉 Jenkins pipelines automate full flow:
Code → Build → Test → Deploy

---

# 3. What is a Jenkins Pipeline?

## Answer
A pipeline is a **set of automated steps defined in a Jenkinsfile to build and deploy applications**.

## Real DevOps Usage
👉 Used to:
- automate deployments
- standardize workflows

---

# 4. What is Jenkinsfile?

## Answer
A Jenkinsfile is a **Groovy-based script that defines pipeline stages**.

Example:
```
pipeline {
  stages {
    stage('Build') {
      steps {
        sh 'mvn clean package'
      }
    }
  }
}
```

---

# 5. What are stages in Jenkins?

## Answer
Stages divide pipeline into logical steps like:

- Build
- Test
- Deploy

## Real DevOps Usage
👉 Helps track pipeline progress and debugging.

---

# 6. What are Jenkins Agents (Nodes)?

## Answer
Agents are **machines where Jenkins jobs run**.

## Real DevOps Usage
👉 Used to:
- distribute workload
- run builds in parallel

---

# 7. What is Jenkins Master?

## Answer
Master is the **main server that manages jobs and agents**.

---

# 8. What are Jenkins Plugins?

## Answer
Plugins extend Jenkins functionality.

Examples:
- Git plugin
- Docker plugin
- Kubernetes plugin

## Real DevOps Usage
👉 Used to integrate tools like:
- GitHub
- AWS
- Docker

---

# 9. What is Freestyle Job?

## Answer
Freestyle job is a **simple Jenkins job with GUI configuration**.

## Real DevOps Usage
👉 Used for basic tasks, but pipelines are preferred.

---

# 10. What is Multibranch Pipeline?

## Answer
Automatically creates pipelines for each Git branch.

## Real DevOps Usage
👉 Used for:
- feature branches
- PR-based workflows

---

# 11. What is Blue-Green Deployment in Jenkins?

## Answer
Deploy two versions:
- Blue (current)
- Green (new)

Switch traffic after testing.

## Real DevOps Usage
👉 Used to achieve zero downtime deployment.

---

# 12. What is Jenkins Workspace?

## Answer
Workspace is the **directory where Jenkins builds code**.

---

# 13. What is a Build Trigger?

## Answer
Triggers start a job automatically.

Types:
- Git webhook
- schedule (cron)
- manual

---

# 14. What is Poll SCM?

## Answer
Jenkins checks Git repo periodically for changes.

---

# 15. What is Webhook in Jenkins?

## Answer
Webhook triggers Jenkins **immediately when code is pushed**.

## Real DevOps Usage
👉 Used in CI pipelines for instant builds.

---

# 16. What are Environment Variables in Jenkins?

## Answer
Variables used in pipelines.

Example:
```
env.BUILD_NUMBER
```

---

# 17. What is Jenkins Credential Management?

## Answer
Stores sensitive data like:

- passwords
- tokens
- SSH keys

## Real DevOps Usage
👉 Used to securely access:
- GitHub
- AWS
- Docker registry

---

# 18. What is Parallel Execution in Jenkins?

## Answer
Runs multiple jobs simultaneously.

## Real DevOps Usage
👉 Used to:
- speed up pipelines
- run tests in parallel

---

# 19. What is Jenkins Integration with Docker?

## Answer
Jenkins builds and runs Docker containers.

## Real DevOps Usage
👉 Used for:
- containerized builds
- consistent environments

---

# 20. Why is Jenkins important for DevOps?

## Answer
Jenkins helps:

- automate pipelines
- improve deployment speed
- reduce human errors
- enable continuous delivery

---

# 🎯 Interview Tip

If asked:

👉 “How do you use Jenkins in your project?”

Say:

- Integrated GitHub with Jenkins  
- Used pipelines for build & deploy  
- Built Docker images  
- Pushed to registry  
- Deployed to Kubernetes  
- Used webhooks for automation  

---

# 🚀 Why This Section is Important

This shows:

✅ CI/CD understanding  
✅ Real project experience  
✅ Automation skills  
✅ DevOps maturity  
