# ⚙ Ansible Scenario-Based DevOps Interview Questions

This section contains **real-world Ansible troubleshooting scenarios** commonly faced by DevOps engineers.

---

# Scenario 1: Ansible Cannot Connect to Remote Server

### Problem
Ansible fails with error:

```
UNREACHABLE! Failed to connect via SSH
```

### Possible Causes

- SSH service not running
- Incorrect SSH key
- Wrong inventory IP address
- Firewall blocking SSH

### Solution

Verify SSH connectivity manually:

```
ssh user@server-ip
```

Check SSH service:

```
systemctl status sshd
```

Ensure correct inventory configuration.

---

# Scenario 2: Playbook Fails on Remote Nodes

### Problem
Playbook execution fails on some servers.

### Possible Causes

- missing package manager
- incorrect module usage
- permission issues

### Solution

Run playbook in verbose mode:

```
ansible-playbook playbook.yml -vvv
```

Check task errors and fix module configuration.

---

# Scenario 3: Handler Not Triggering

### Problem
Handler defined in playbook is not running.

### Cause

Handlers run only when **a task reports changes**.

### Solution

Ensure task includes:

```
notify: restart nginx
```

Example:

```
- name: update nginx config
  template:
    src: nginx.conf.j2
    dest: /etc/nginx/nginx.conf
  notify: restart nginx
```

---

# Scenario 4: Inventory Not Detecting Hosts

### Problem
Ansible cannot detect hosts in inventory.

### Possible Causes

- incorrect inventory format
- wrong group names
- syntax error

### Solution

Verify inventory:

```
ansible-inventory --list
```

Example inventory:

```
[webservers]
192.168.1.10
192.168.1.11
```

---

# Scenario 5: Playbook Running But No Changes Applied

### Problem
Playbook executes successfully but nothing changes.

### Cause

Ansible is idempotent and system already matches desired state.

### Solution

Check task conditions and configuration.

Use:

```
--check
```

to preview changes.

---

# Scenario 6: Package Installation Fails

### Problem
Ansible fails to install packages.

### Possible Causes

- package repository not updated
- wrong package name
- permission issue

### Solution

Update repository before installation.

Example:

```
- name: update apt repo
  apt:
    update_cache: yes
```

---

# Scenario 7: Variables Not Working in Playbook

### Problem
Variables not being applied correctly.

### Cause

Incorrect variable definition or scope.

### Solution

Check variable files:

```
vars/
group_vars/
host_vars/
```

Ensure proper variable syntax.

---

# Scenario 8: Playbook Takes Too Long

### Problem
Playbook execution is slow when managing many servers.

### Solution

Use **parallel execution**.

Increase forks value in configuration:

```
forks = 10
```

in:

```
ansible.cfg
```

---

# Scenario 9: Sensitive Data Exposed in Playbook

### Problem
Passwords or API keys stored in plain text.

### Solution

Use **Ansible Vault**.

Example:

```
ansible-vault encrypt secrets.yml
```

This secures sensitive information.

---

# Scenario 10: Need Reusable Configuration for Multiple Servers

### Problem
Multiple servers require the same configuration.

### Solution

Use **Ansible Roles**.

Example role structure:

```
roles/
   webserver/
       tasks/
       handlers/
       templates/
       vars/
```

Roles help organize and reuse automation code.

---

# 🎯 Why Ansible Scenarios Are Important for DevOps

DevOps engineers use Ansible for:

- server configuration
- application deployment
- infrastructure automation
- environment consistency

Understanding these troubleshooting scenarios helps maintain **reliable automated infrastructure**.
