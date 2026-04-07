# 👤 Linux Users, Groups, Permissions & Umask – DevOps Interview Guide

---

# 🧠 1. Users in Linux

Linux is a **multi-user system**, where multiple users can access the same system with controlled permissions.

---

## 👥 Types of Users

| Type        | Description                            |
| ----------- | -------------------------------------- |
| Root User   | Superuser with full access (UID = 0)   |
| System User | Used by services (e.g., nginx, docker) |
| Normal User | Regular login users                    |

---

## 🔍 Important Files

* `/etc/passwd` → user details
* `/etc/shadow` → encrypted passwords
* `/etc/group` → group info

---

## ⚙️ User Management Commands

```bash id="x6q3fg"
useradd username
passwd username
usermod -aG group username
userdel username
id username
```

---

# 👨‍👩‍👧‍👦 2. Groups in Linux

Groups are used to **manage permissions for multiple users efficiently**.

---

## 📂 Types of Groups

* Primary Group → assigned at user creation
* Secondary Group → additional access

---

## 🔍 Group Commands

```bash id="m4pkj1"
groupadd devops
groupdel devops
usermod -aG devops username
groups username
```

---

# 🔐 3. File Permissions in Linux

---

## 📌 Permission Types

| Symbol | Meaning |
| ------ | ------- |
| r      | Read    |
| w      | Write   |
| x      | Execute |

---

## 👥 Permission Categories

* User (Owner)
* Group
* Others

---

## 🔍 View Permissions

```bash id="q1t5jp"
ls -l
```

👉 Example:

```id="npx2k3"
-rwxr-xr-- file.sh
```

Breakdown:

* `rwx` → user
* `r-x` → group
* `r--` → others

---

## 🔢 Numeric (Octal) Permissions

| Permission | Value |
| ---------- | ----- |
| r          | 4     |
| w          | 2     |
| x          | 1     |

👉 Example:

```bash id="w9v9gl"
chmod 755 file.sh
```

---

## ⚙️ Change Permissions

```bash id="c3w3fy"
chmod +x file.sh
chmod 644 file.txt
chown user:group file
```

---

# 🎭 4. Special Permissions

---

## 🔥 Types

| Permission | Meaning                |
| ---------- | ---------------------- |
| SUID       | Run as file owner      |
| SGID       | Run as group           |
| Sticky Bit | Restrict file deletion |

---

## 🔍 Example

```bash id="v9n8px"
chmod +s file
chmod 1777 /tmp
```

---

# 🧮 5. Umask (Default Permissions)

---

## 🧠 What is Umask?

Umask defines **default permissions for new files and directories**.

---

## 📌 Default Values

* Files → 666
* Directories → 777

---

## 🔢 Formula

👉 Final Permission = Default - Umask

---

## 🔍 Example

```bash id="x8y0jd"
umask 022
```

* File → 644
* Directory → 755

---

## 🔍 Check Umask

```bash id="c9l2op"
umask
```

---

# 🚀 DevOps Practical Usage

---

## 📌 Where You’ll Use This:

* Managing access for teams
* Securing application files
* Setting permissions for logs/configs
* Docker & Kubernetes volume permissions

---

## 🔥 Real Scenario

👉 App not working due to permission denied

**Solution:**

```bash id="l3s8yt"
chmod +x script.sh
chown appuser:appgroup file
```

---

## 🔥 Scenario 2

👉 Multiple users need access to same directory

**Solution:**

```bash id="t6h9av"
chgrp devops /project
chmod 770 /project
```

---

# 🔥 Interview Questions & Answers

---

## ❓ 1. What are users in Linux?

**Answer:**
Users are accounts that can log into the system. Each user has a unique UID and permissions.

---

## ❓ 2. What is the difference between root and normal user?

**Answer:**

* Root → full access
* Normal user → limited access

---

## ❓ 3. What are groups?

**Answer:**
Groups are collections of users used to manage permissions efficiently.

---

## ❓ 4. What are file permissions?

**Answer:**
Permissions define access levels (read, write, execute) for user, group, and others.

---

## ❓ 5. What does chmod 777 mean?

**Answer:**
Full permissions (read, write, execute) for everyone.

---

## ❓ 6. What is umask?

**Answer:**
Umask defines default permissions for newly created files and directories.

---

## ❓ 7. How do you change file ownership?

```bash id="qv0b2k"
chown user:group file
```

---

## ❓ 8. What is SUID?

**Answer:**
Allows a file to run with the permissions of the file owner.

---

## ❓ 9. What is sticky bit?

**Answer:**
Prevents users from deleting others’ files in shared directories (like `/tmp`).

---

## ❓ 10. How do you check user details?

```bash id="r7p1mn"
id username
```

---

# ⚙️ Important Commands

```bash id="x2n7cv"
useradd, userdel, usermod
groupadd, groupdel
chmod, chown, chgrp
umask
ls -l
```

---

# 🎯 Pro Tips for DevOps Interview

* Always explain with **real scenarios**
* Focus on:

  * Permission denied issues
  * Shared directories
  * Secure configs
* Avoid giving 777 in production ❌

---

# ✅ One-Line Summary

👉 *Linux uses users, groups, and permissions to control access, while umask defines default permissions for new files.*

---

# ⭐ Use This Repo For

* DevOps Interview Preparation
* Linux Fundamentals
* Production Troubleshooting

---

🔥 **Pro Tip:** Practice by creating users, groups, and testing permissions in a real Linux system.

---
