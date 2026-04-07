# 📁 Linux File System Hierarchy – DevOps Interview Q&A (2 Years Experience)

---

## 🧠 What is Linux File System Hierarchy?

The Linux File System Hierarchy follows the **Filesystem Hierarchy Standard (FHS)**, which defines how directories are structured and used in Linux systems.

👉 Everything starts from the root directory `/`, and all files and directories are organized under it.

---

## 📂 Important Directories Explained

| Directory | Purpose                         |
| --------- | ------------------------------- |
| `/`       | Root directory (base of system) |
| `/home`   | User home directories           |
| `/root`   | Root user home                  |
| `/etc`    | Configuration files             |
| `/bin`    | Essential commands              |
| `/sbin`   | System/admin commands           |
| `/usr`    | Applications & libraries        |
| `/var`    | Logs & variable data            |
| `/tmp`    | Temporary files                 |
| `/dev`    | Device files                    |
| `/proc`   | Process/system info             |
| `/opt`    | Optional software               |
| `/boot`   | Boot files                      |

---

# 🔥 Interview Questions & Answers

---

## ❓ 1. What is the Linux File System Hierarchy?

**Answer:**
Linux uses a hierarchical structure starting from `/` (root). It organizes system files, user data, applications, and configurations into standardized directories like `/etc`, `/var`, and `/usr`.

---

## ❓ 2. What is the purpose of `/etc`?

**Answer:**
`/etc` contains all system-wide configuration files.

👉 Examples:

* `/etc/passwd` → user details
* `/etc/hosts` → hostname mapping
* `/etc/ssh/sshd_config` → SSH config

---

## ❓ 3. What is the difference between `/bin` and `/usr/bin`?

**Answer:**

* `/bin` → essential commands required for system boot (ls, cp, bash)
* `/usr/bin` → additional user-installed commands

👉 Modern systems may merge them, but conceptually they differ.

---

## ❓ 4. What is `/var` used for?

**Answer:**
Stores variable data like logs, cache, and spool files.

👉 Important:

* `/var/log` → system & application logs

---

## ❓ 5. Where are logs stored in Linux?

**Answer:**
Logs are stored in:

```
/var/log
```

👉 Example:

* `/var/log/syslog`
* `/var/log/messages`
* `/var/log/nginx/access.log`

---

## ❓ 6. What is `/proc`?

**Answer:**
A virtual filesystem that provides real-time system and process information.

👉 Examples:

```
/proc/cpuinfo
/proc/meminfo
```

---

## ❓ 7. What is `/dev`?

**Answer:**
Contains device files representing hardware.

👉 Examples:

* `/dev/sda` → disk
* `/dev/null` → discards output

---

## ❓ 8. What is `/tmp`?

**Answer:**
Stores temporary files. Usually cleared on reboot.

---

## ❓ 9. What is mounting in Linux?

**Answer:**
Mounting is the process of attaching a filesystem to a directory.

👉 Example:

```bash
mount /dev/sdb1 /mnt
```

---

## ❓ 10. What is `/opt` used for?

**Answer:**
Used for installing third-party or optional software.

👉 Example:

```
/opt/tomcat
```

---

# 🚀 DevOps Scenario-Based Questions

---

## ❓ 11. Your application is not working. Where will you check logs?

**Answer:**

```
/var/log
```

Also check application-specific logs (e.g., `/var/log/nginx/`, `/var/log/docker/`)

---

## ❓ 12. You need to change a service configuration. Where will you go?

**Answer:**

```
/etc
```

---

## ❓ 13. Disk is full. How will you troubleshoot?

**Answer:**

```bash
df -h        # check disk usage
du -sh /*    # check directory sizes
```

👉 Focus on:

* `/var/log`
* `/tmp`

---

## ❓ 14. How do you find large files?

**Answer:**

```bash
find / -type f -size +100M
```

---

## ❓ 15. How do you check memory and CPU info?

**Answer:**

```bash
cat /proc/meminfo
cat /proc/cpuinfo
```

---

# ⚙️ Important Commands for DevOps

```bash
ls        # list files
cd        # change directory
pwd       # current path
df -h     # disk usage
du -sh    # directory size
mount     # mount filesystem
umount    # unmount
cat       # view file
less      # read large files
```

---

# 🎯 Pro Tips for Interview

* Always mention **real-world usage**
* Focus on:

  * `/var/log` (logs)
  * `/etc` (configs)
  * `/usr` & `/opt` (apps)
* Explain with examples (very important)

---

# ✅ One-Line Summary

👉 *Linux file system hierarchy organizes all files starting from root (`/`) into structured directories like `/etc`, `/var`, and `/usr`, making system management efficient.*

---

# ⭐ Use This Repo For

* DevOps Interview Preparation
* Linux Basics Revision
* Real-world Troubleshooting

---

🔥 **Pro Tip:** Practice commands daily + explore `/var/log` on real servers.

---
