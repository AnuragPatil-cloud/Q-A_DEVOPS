# 🔍 SonarQube Interview Questions & Answers (DevOps)

This section contains commonly asked **SonarQube interview questions for DevOps Engineers (Fresher – 2+ Years Experience).**

---

# 1. What is SonarQube?

SonarQube is an **open-source code quality and security analysis tool** used to inspect source code and identify issues such as:

- Bugs
- Code smells
- Security vulnerabilities
- Duplicated code

It helps improve **code quality and maintainability**.

---

# 2. Why do we use SonarQube?

SonarQube is used to:

- Improve code quality
- Detect security vulnerabilities
- Identify bugs in code
- Maintain coding standards
- Monitor technical debt

---

# 3. What is Static Code Analysis?

Static code analysis is the process of **analyzing source code without executing the program**.

It helps detect issues early in the development process.

---

# 4. What are the main components of SonarQube?

SonarQube architecture includes:

- SonarQube Server
- SonarQube Scanner
- Database
- Web Interface

---

# 5. What is SonarQube Scanner?

SonarQube Scanner is a **tool used to analyze source code and send the results to the SonarQube server.**

Example command:

```
sonar-scanner
```

---

# 6. What is a Quality Gate?

A Quality Gate is a **set of conditions that code must meet before it is considered acceptable.**

Example conditions:

- No critical vulnerabilities
- Code coverage > 80%
- No new bugs

If conditions fail, the pipeline can be stopped.

---

# 7. What are Code Smells?

Code smells are **poor coding practices that affect code readability and maintainability**.

Examples:

- Duplicate code
- Large functions
- Complex logic

---

# 8. What are Bugs in SonarQube?

Bugs are **coding errors that may cause incorrect behavior in the application.**

Example:

- Null pointer exception
- Incorrect logic

---

# 9. What are Vulnerabilities?

Vulnerabilities are **security issues that attackers could exploit.**

Examples:

- SQL injection
- Cross-site scripting (XSS)
- Hardcoded credentials

---

# 10. What is Technical Debt?

Technical debt refers to **the cost of fixing code issues later due to poor coding practices today.**

SonarQube estimates the effort required to fix issues.

---

# 11. What is Code Coverage?

Code coverage measures **how much of the code is tested by automated tests.**

Example:

```
80% code coverage
```

---

# 12. What is SonarQube Dashboard?

The SonarQube dashboard displays:

- Code quality metrics
- Bugs
- Vulnerabilities
- Code smells
- Coverage reports

---

# 13. What is SonarQube Default Port?

Default port:

```
9000
```

Example access:

```
http://server-ip:9000
```

---

# 14. How does SonarQube integrate with Jenkins?

Typical pipeline:

1. Developer pushes code to Git
2. Jenkins triggers build
3. SonarQube scans the code
4. Quality Gate checks results
5. Deployment continues if checks pass

---

# 15. Example SonarQube Jenkins Pipeline Step

```
sonar-scanner \
  -Dsonar.projectKey=myproject \
  -Dsonar.sources=. \
  -Dsonar.host.url=http://localhost:9000 \
  -Dsonar.login=token
```

---

# 16. Supported Programming Languages in SonarQube

SonarQube supports many languages such as:

- Java
- Python
- JavaScript
- C#
- Go
- PHP

---

# 17. Real DevOps Scenario

### Problem

Application code has many security vulnerabilities.

### Solution

Run SonarQube analysis in the CI/CD pipeline to detect and fix issues before deployment.

---

# 18. Benefits of SonarQube

- Improves code quality
- Detects security vulnerabilities
- Integrates with CI/CD pipelines
- Supports multiple languages
- Provides detailed reports

---

# 🚀 Why SonarQube is Important for DevOps

SonarQube helps DevOps teams:

- Maintain code quality
- Detect security issues early
- Automate code analysis
- Enforce coding standards

Common integrations:

- Jenkins
- GitHub
- GitLab
- Docker
- Kubernetes
