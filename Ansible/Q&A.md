# ⚙ Ansible Interview Questions & Answers (DevOps)

This section contains commonly asked **Ansible interview questions** for DevOps engineers.

---

# 1. What is Ansible?

Ansible is an **open-source configuration management and automation tool used to automate IT tasks such as server configuration, application deployment, and infrastructure management**.

It helps automate repetitive tasks in DevOps environments.

---

# 2. What are the main features of Ansible?

Key features of Ansible include:

- Agentless architecture
- Simple YAML-based configuration
- Easy automation
- Idempotent operations
- SSH-based communication

---

# 3. What is Ansible used for?

Ansible is used for:

- configuration management
- application deployment
- infrastructure automation
- orchestration
- provisioning cloud resources

---

# 4. What is an Ansible Playbook?

A playbook is a **YAML file containing a set of automation tasks executed on remote systems**.

Example structure:

```
hosts
tasks
modules
```

Playbooks define how systems should be configured.

---

# 5. What is an Ansible Inventory?

Inventory is a **list of hosts or servers that Ansible manages**.

Example:

```
[webservers]
192.168.1.10
192.168.1.11
```

Inventory can be:

- static
- dynamic

---

# 6. What are Ansible Modules?

Modules are **prebuilt programs used by Ansible to perform tasks on remote systems**.

Examples:

- yum
- apt
- copy
- service
- file

---

# 7. What is an Ansible Role?

Roles are used to **organize playbooks into reusable components**.

Typical role structure includes:

```
tasks
handlers
templates
files
vars
defaults
```

---

# 8. What is Idempotency in Ansible?

Idempotency means **running the same playbook multiple times will not change the system if it is already in the desired state**.

Example:

If a package is already installed, Ansible will not install it again.

---

# 9. What is an Ansible Handler?

Handlers are **tasks that run only when notified by another task**.

They are commonly used to restart services.

Example:

```
notify: restart nginx
```

---

# 10. What is Ansible Ad-Hoc Command?

Ad-hoc commands are **one-line commands used to perform quick tasks without writing a playbook**.

Example:

```
ansible all -m ping
```

---

# 11. What is YAML in Ansible?

YAML (Yet Another Markup Language) is the **format used to write Ansible playbooks**.

Example:

```
- hosts: webservers
  tasks:
    - name: install nginx
      apt:
        name: nginx
        state: present
```

---

# 12. What is Ansible Control Node?

The control node is the **machine where Ansible is installed and from which automation tasks are executed**.

It manages remote nodes.

---

# 13. What are Managed Nodes?

Managed nodes are the **remote servers that Ansible manages and configures**.

These nodes do not require Ansible to be installed.

---

# 14. What is Dynamic Inventory?

Dynamic inventory automatically **fetches server information from cloud providers like AWS, Azure, or GCP**.

Example:

```
AWS EC2 instances automatically added to inventory
```

---

# 15. What is Ansible Vault?

Ansible Vault is used to **encrypt sensitive data such as passwords, API keys, and secrets**.

Example:

```
ansible-vault encrypt secrets.yml
```

---

# 16. What is a Template in Ansible?

Templates allow **dynamic configuration files using Jinja2 templating engine**.

Example:

```
nginx.conf.j2
```

Variables can be inserted into configuration files.

---

# 17. What is Ansible Galaxy?

Ansible Galaxy is a **repository where users can share and download Ansible roles**.

It helps reuse automation components.

---

# 18. What is the difference between Ansible and Puppet?

| Feature | Ansible | Puppet |
|---|---|---|
Architecture | Agentless | Agent-based |
Language | YAML | Puppet DSL |
Communication | SSH | SSL |

---

# 19. What are common Ansible modules?

Common modules include:

- apt
- yum
- service
- copy
- file
- user
- command
- shell

---

# 20. Why is Ansible important for DevOps?

Ansible helps DevOps teams:

- automate server configuration
- deploy applications
- manage infrastructure
- reduce manual effort
- ensure consistent environments
