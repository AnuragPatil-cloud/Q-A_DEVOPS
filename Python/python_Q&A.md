# 🐍 Python for DevOps Interview Questions & Answers

This section contains commonly asked **Python interview questions for DevOps Engineers (Fresher – 2+ Years Experience).**

Python is widely used in DevOps for **automation, scripting, infrastructure management, and CI/CD pipelines.**

---

# 1. Why is Python used in DevOps?

Python is popular in DevOps because:

- Easy to learn
- Strong automation capabilities
- Large library ecosystem
- Good integration with cloud APIs

Common uses:

- Infrastructure automation
- CI/CD scripts
- Monitoring tools
- Cloud automation

---

# 2. What are Python modules?

A module is a **file containing Python code such as functions, classes, or variables**.

Example:

```
import os
import sys
```

---

# 3. What are Python libraries used in DevOps?

Common DevOps Python libraries:

- boto3 → AWS automation
- requests → API calls
- paramiko → SSH automation
- subprocess → run system commands
- docker → Docker API integration

---

# 4. What is PIP?

PIP is the **package manager for Python used to install libraries**.

Example:

```
pip install boto3
```

---

# 5. What is a Virtual Environment?

A virtual environment is an **isolated environment used to manage project dependencies separately.**

Example:

```
python3 -m venv venv
source venv/bin/activate
```

---

# 6. How do you run system commands in Python?

Example:

```python
import os

os.system("ls")
```

Using subprocess:

```python
import subprocess

subprocess.run(["ls", "-l"])
```

---

# 7. Example Python Script for Automation

Example script to check disk usage:

```python
import shutil

total, used, free = shutil.disk_usage("/")

print("Total:", total)
print("Used:", used)
print("Free:", free)
```

---

# 8. What is JSON in Python?

JSON is a **data format commonly used in APIs and configuration files**.

Example:

```python
import json

data = '{"name":"DevOps"}'
obj = json.loads(data)

print(obj["name"])
```

---

# 9. How does Python interact with APIs?

Using the `requests` library.

Example:

```python
import requests

response = requests.get("https://api.github.com")

print(response.status_code)
```

---

# 10. What is boto3?

boto3 is the **AWS SDK for Python** used to interact with AWS services.

Example:

```python
import boto3

ec2 = boto3.client('ec2')
response = ec2.describe_instances()

print(response)
```

---

# 11. What is Paramiko?

Paramiko is a **Python library used to connect to remote servers via SSH**.

Example:

```python
import paramiko

ssh = paramiko.SSHClient()
ssh.set_missing_host_key_policy(paramiko.AutoAddPolicy())
ssh.connect("server_ip", username="user", password="pass")
```

---

# 12. Example Python Script for Server Monitoring

```python
import psutil

cpu = psutil.cpu_percent()
memory = psutil.virtual_memory().percent

print("CPU Usage:", cpu)
print("Memory Usage:", memory)
```

---

# 13. What is Logging in Python?

Logging helps track events and errors in applications.

Example:

```python
import logging

logging.basicConfig(level=logging.INFO)
logging.info("Script started")
```

---

# 14. What is Exception Handling?

Exception handling prevents program crashes.

Example:

```python
try:
    x = 10 / 0
except Exception as e:
    print("Error:", e)
```

---

# 15. Real DevOps Scenario

### Problem

You need to create multiple EC2 instances automatically.

### Solution

Use a Python script with **boto3** to automate AWS resource creation.

---

# 16. Benefits of Python in DevOps

- Infrastructure automation
- Cloud resource management
- API integrations
- Monitoring scripts
- CI/CD automation

---

# 🚀 Why Python is Important for DevOps

Python is widely used for:

- Automation scripts
- Cloud automation
- Infrastructure management
- Monitoring tools

Popular DevOps tools written in Python:

- Ansible
- SaltStack
- AWS CLI
- OpenStack
