# ⚙️ Ansible Interview Questions & Answers (DevOps)

This section contains commonly asked **Ansible interview questions for DevOps Engineers (Fresher – 2+ Years Experience).**

---

# 1. What is Ansible?

Ansible is an **open-source configuration management and automation tool** used for:

- Application deployment
- Configuration management
- Infrastructure automation
- Orchestration

It works using **SSH and does not require any agent installation on target machines.**

---

# 2. Why do we use Ansible?

Ansible helps in:

- Automating repetitive tasks
- Managing multiple servers
- Application deployment
- Configuration management
- Infrastructure provisioning

---

# 3. What is Configuration Management?

Configuration management is the process of **maintaining systems in a desired and consistent state automatically**.

Example tools:

- Ansible
- Puppet
- Chef
- SaltStack

---

# 4. What is Ansible Architecture?

Ansible uses a **simple architecture**:

Control Node  
The machine where Ansible is installed.

Managed Nodes  
The servers that Ansible manages through SSH.

Inventory  
File containing the list of target servers.

Playbooks  
YAML files that define automation tasks.

---

# 5. What is an Inventory in Ansible?

An inventory file contains **a list of servers that Ansible will manage**.

Example:

```
[webservers]
192.168.1.10
192.168.1.11

[dbservers]
192.168.1.20
```

---

# 6. What is a Playbook?

A playbook is a **YAML file used to define automation tasks in Ansible**.

Example playbook:

```yaml
- name: Install nginx
  hosts: webservers
  become: yes

  tasks:
    - name: Install nginx package
      apt:
        name: nginx
        state: present
```

---

# 7. What are Ansible Modules?

Modules are **small programs used to perform specific tasks on managed nodes**.

Common modules:

- apt
- yum
- copy
- file
- service
- user
- package

Example:

```yaml
- name: Install nginx
  apt:
    name: nginx
    state: present
```

---

# 8. What is an Ansible Role?

Roles are used to **organize playbooks and tasks into reusable components**.

Example structure:

```
roles/
  webserver/
    tasks/
    handlers/
    templates/
    files/
    vars/
```

---

# 9. What are Ansible Tasks?

Tasks are **individual operations performed in a playbook**.

Example:

```yaml
tasks:
  - name: Start nginx service
    service:
      name: nginx
      state: started
```

---

# 10. What are Ansible Handlers?

Handlers are **tasks that run only when triggered by a notification**.

Example:

```yaml
tasks:
  - name: Copy config file
    copy:
      src: nginx.conf
      dest: /etc/nginx/nginx.conf
    notify: restart nginx

handlers:
  - name: restart nginx
    service:
      name: nginx
      state: restarted
```

---

# 11. What are Ansible Variables?

Variables allow **dynamic values in playbooks**.

Example:

```yaml
vars:
  package_name: nginx
```

Use variable:

```yaml
name: "{{ package_name }}"
```

---

# 12. What are Ansible Facts?

Facts are **system information collected by Ansible from managed nodes**.

Example:

- IP address
- OS version
- Memory

Command:

```
ansible all -m setup
```

---

# 13. What is Idempotency in Ansible?

Idempotency means **running the same playbook multiple times will not change the system if it is already in the desired state.**

Example:

If nginx is already installed, Ansible will not install it again.

---

# 14. Important Ansible Commands

```
ansible --version
ansible all -m ping
ansible-playbook playbook.yml
ansible-inventory --list
ansible-doc module_name
```

---

# 15. How do you test Ansible connectivity?

```
ansible all -m ping
```

---

# 16. How do you run an Ansible playbook?

```
ansible-playbook playbook.yml
```

---

# 17. What is Ansible Galaxy?

Ansible Galaxy is a **repository for sharing Ansible roles**.

Example:

```
ansible-galaxy install geerlingguy.nginx
```

---

# 18. What is YAML in Ansible?

YAML is a **human-readable data format used to write Ansible playbooks**.

Rules:

- Uses indentation
- Key-value format
- No tabs allowed

Example:

```
name: nginx
state: present
```

---

# 19. Real DevOps Scenario

### Problem

You need to install nginx on **50 servers**.

### Solution

Use Ansible playbook to install nginx on all servers automatically.

Example:

```
ansible-playbook install-nginx.yml
```

Benefits:

- Faster deployment
- No manual login to servers
- Consistent configuration

---

# 20. Why Ansible is Important for DevOps

Ansible helps DevOps teams:

- Automate server configuration
- Deploy applications
- Manage infrastructure
- Maintain consistency across environments

Ansible integrates with:

- AWS
- Docker
- Kubernetes
- Terraform
- Jenkins
