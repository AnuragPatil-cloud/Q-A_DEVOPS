# ⚡ GitHub Actions Interview Questions & Answers (DevOps)

This section contains commonly asked **GitHub Actions interview questions for DevOps Engineers (Fresher – 2+ Years Experience).**

---

# 1. What is GitHub Actions?

GitHub Actions is a **CI/CD automation tool provided by GitHub** that allows you to build, test, and deploy code directly from your GitHub repository.

It helps automate workflows such as:

- Building applications
- Running tests
- Deploying applications
- Running scripts automatically

---

# 2. What is CI/CD in GitHub Actions?

CI (Continuous Integration)  
Automatically build and test code whenever developers push code to the repository.

CD (Continuous Deployment / Delivery)  
Automatically deploy the application after successful builds and tests.

---

# 3. What is a Workflow in GitHub Actions?

A workflow is an **automated process defined in a YAML file**.

Workflows run when certain events occur.

Example events:

- Push
- Pull request
- Scheduled time

Workflow files are stored in:

```
.github/workflows/
```

---

# 4. What is a GitHub Actions Workflow File?

A workflow file is a **YAML file that defines automation steps**.

Example:

```yaml
name: CI Pipeline

on: push

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout Code
        uses: actions/checkout@v3

      - name: Run Script
        run: echo "Hello DevOps"
```

---

# 5. What are Events in GitHub Actions?

Events are **triggers that start a workflow**.

Common events:

- push
- pull_request
- workflow_dispatch
- schedule

Example:

```yaml
on: push
```

---

# 6. What are Jobs in GitHub Actions?

Jobs are **sets of steps that run on the same runner**.

Example:

```yaml
jobs:
  build:
    runs-on: ubuntu-latest
```

---

# 7. What are Steps in GitHub Actions?

Steps are **individual tasks inside a job**.

Example:

```yaml
steps:
  - name: Install dependencies
    run: npm install
```

---

# 8. What is a Runner in GitHub Actions?

A runner is the **server that runs the GitHub Actions workflow**.

Types of runners:

- GitHub-hosted runners
- Self-hosted runners

Example:

```
runs-on: ubuntu-latest
```

---

# 9. What are GitHub Actions?

Actions are **reusable automation units used in workflows**.

Example:

```
actions/checkout
```

This action checks out repository code.

Example usage:

```yaml
uses: actions/checkout@v3
```

---

# 10. What are Environment Variables in GitHub Actions?

Environment variables store values used during workflow execution.

Example:

```yaml
env:
  APP_NAME: myapp
```

---

# 11. What are Secrets in GitHub Actions?

Secrets store **sensitive information such as passwords or API keys**.

Examples:

- AWS credentials
- Docker Hub password
- API tokens

Access secrets:

```yaml
${{ secrets.AWS_ACCESS_KEY }}
```

---

# 12. What is Matrix Strategy in GitHub Actions?

Matrix strategy allows **running jobs across multiple environments simultaneously**.

Example:

```yaml
strategy:
  matrix:
    node-version: [14, 16, 18]
```

---

# 13. How do you manually trigger a workflow?

Use:

```
workflow_dispatch
```

Example:

```yaml
on:
  workflow_dispatch:
```

---

# 14. What is a Scheduled Workflow?

A scheduled workflow runs automatically at a specific time using **cron syntax**.

Example:

```yaml
on:
  schedule:
    - cron: "0 2 * * *"
```

Runs every day at **2 AM**.

---

# 15. Example CI Pipeline using GitHub Actions

```yaml
name: CI Pipeline

on:
  push:
    branches:
      - main

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout Code
        uses: actions/checkout@v3

      - name: Install Dependencies
        run: npm install

      - name: Run Tests
        run: npm test
```

---

# 16. Real DevOps CI/CD Scenario

Example pipeline:

1. Developer pushes code to GitHub
2. GitHub Actions triggers workflow
3. Application is built
4. Tests are executed
5. Docker image is created
6. Image pushed to registry
7. Application deployed to Kubernetes

---

# 17. Example Docker Build using GitHub Actions

```yaml
- name: Build Docker Image
  run: docker build -t myapp .
```

---

# 18. Example Docker Push using GitHub Actions

```yaml
- name: Push Docker Image
  run: docker push myrepo/myapp
```

---

# 19. Benefits of GitHub Actions

- Built into GitHub
- Easy CI/CD setup
- Supports automation workflows
- Large marketplace of actions
- Integration with DevOps tools

---

# 20. GitHub Actions Integration

GitHub Actions integrates with:

- Docker
- Kubernetes
- AWS
- Terraform
- Azure
- Google Cloud
