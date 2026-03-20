# 🚀 GitHub Actions Interview Questions & Answers (DevOps)

This section contains commonly asked **GitHub Actions interview questions** for DevOps engineers.

---

# 1. What is GitHub Actions?

GitHub Actions is a **CI/CD (Continuous Integration and Continuous Deployment) tool provided by GitHub to automate workflows such as build, test, and deployment**.

---

# 2. What is a Workflow in GitHub Actions?

A workflow is a **YAML file that defines automation steps**.

It is stored in:

```
.github/workflows/
```

---

# 3. What is a Job in GitHub Actions?

A job is a **set of steps executed on the same runner**.

A workflow can have multiple jobs.

---

# 4. What is a Step in GitHub Actions?

A step is an **individual task executed within a job**.

Example:

- run a command
- use an action

---

# 5. What is a Runner?

A runner is a **server that executes GitHub Actions workflows**.

Types:

- GitHub-hosted runners
- Self-hosted runners

---

# 6. What is an Action?

An action is a **reusable unit of code used within workflows**.

Example:

```
uses: actions/checkout@v3
```

---

# 7. What triggers a GitHub Actions workflow?

Workflows can be triggered by events such as:

- push
- pull request
- schedule
- manual trigger (workflow_dispatch)

---

# 8. What is a YAML file in GitHub Actions?

YAML is used to **define workflows, jobs, and steps**.

Example:

```
name: CI Pipeline
on: push
jobs:
  build:
    runs-on: ubuntu-latest
```

---

# 9. What is the difference between CI and CD?

| CI | CD |
|---|---|
Build and test code | Deploy application |
Ensures code quality | Ensures delivery |

---

# 10. What are environment variables in GitHub Actions?

Environment variables store **configuration values used in workflows**.

Example:

```
env:
  APP_ENV: production
```

---

# 11. What are secrets in GitHub Actions?

Secrets are used to **store sensitive data such as API keys and passwords securely**.

Example:

```
${{ secrets.API_KEY }}
```

---

# 12. What is matrix strategy in GitHub Actions?

Matrix strategy allows running **jobs with multiple configurations**.

Example:

```
strategy:
  matrix:
    node-version: [14, 16]
```

---

# 13. What is caching in GitHub Actions?

Caching improves performance by **storing dependencies between workflow runs**.

Example:

```
uses: actions/cache@v3
```

---

# 14. What is artifact in GitHub Actions?

Artifacts are **files generated during workflow execution and stored for later use**.

Example:

- build files
- logs

---

# 15. What is workflow_dispatch?

workflow_dispatch allows **manual triggering of workflows from GitHub UI**.

---

# 16. What is job dependency in GitHub Actions?

Jobs can depend on each other using:

```
needs:
```

Example:

```
job2:
  needs: job1
```

---

# 17. What is concurrency in GitHub Actions?

Concurrency controls **how many workflow runs execute simultaneously**.

---

# 18. What is self-hosted runner?

A self-hosted runner is a **custom server managed by the user to run workflows**.

---

# 19. What are common use cases of GitHub Actions?

- CI/CD pipelines
- automated testing
- code deployment
- infrastructure automation

---

# 20. Why is GitHub Actions important for DevOps?

GitHub Actions helps DevOps teams:

- automate workflows
- integrate CI/CD pipelines
- improve deployment speed
- reduce manual effort
