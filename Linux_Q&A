# 🐧 Linux Interview Questions & Answers (DevOps)

This section contains commonly asked Linux interview questions for DevOps Engineers (Fresher – 2 Years Experience).

---

# 1. Basic Linux Questions (Freshers)

### 1. What is Linux?
Linux is an open-source operating system kernel based on Unix. It is widely used in servers, cloud platforms, and DevOps environments.

### 2. What is the Linux Kernel?
The kernel is the core part of the Linux operating system that manages:
- CPU
- Memory
- Devices
- Processes

### 3. What are the main components of Linux?
Main components include:
- Kernel
- Shell
- File System
- System Utilities
- Hardware

### 4. What is Shell in Linux?
A shell is a command-line interface that allows users to interact with the Linux operating system.

Examples:
- Bash
- Sh
- Zsh
- Ksh

### 5. What is the root user?
The root user is the superuser in Linux who has full access to all files and commands.

### 6. What is the difference between su and sudo?

su  
Switch user

sudo  
Execute command with superuser privileges

Example:

```bash
sudo apt update
```

### 7. What are Linux file permissions?

Linux permissions control who can read, write, or execute files.

Permission types:
- Read (r)
- Write (w)
- Execute (x)

Example:

```
-rwxr-xr--
```

### 8. What is chmod?

chmod changes file permissions.

Example:

```bash
chmod 755 file.sh
```

### 9. What is chown?

chown changes file ownership.

Example:

```bash
chown user:group file.txt
```

### 10. Important Linux directories

/       Root directory  
/home   User home directories  
/etc    Configuration files  
/var    Logs and variable data  
/bin    Basic commands  
/tmp    Temporary files  

---

# 2. Intermediate Linux Questions (1–2 Years Experience)

### 11. What is a process in Linux?

A process is a running instance of a program.

Example:

```bash
ps -ef
```

### 12. What is PID?

PID stands for Process ID. It uniquely identifies a running process.

### 13. How do you kill a process?

```bash
kill PID
```

Force kill:

```bash
kill -9 PID
```

### 14. Difference between kill and kill -9

kill  
Graceful termination

kill -9  
Forceful termination

### 15. What is top command?

top displays real-time system processes, CPU usage, and memory usage.

### 16. What is df command?

Shows disk space usage.

```bash
df -h
```

### 17. What is du command?

Shows directory size usage.

```bash
du -sh foldername
```

### 18. Difference between soft link and hard link

Hard Link
- Same inode
- Cannot link directories
- Works even if original file deleted

Soft Link
- Different inode
- Can link directories
- Breaks if original file deleted

### 19. How to check memory usage?

```bash
free -m
```

### 20. How to check CPU usage?

```bash
top
```

or

```bash
htop
```

---

# 3. Linux Networking Questions

### 21. How do you check IP address?

```bash
ip a
```

or

```bash
ifconfig
```

### 22. How do you test network connectivity?

```bash
ping google.com
```

### 23. What is SSH?

SSH (Secure Shell) is used to connect securely to remote servers.

Example:

```bash
ssh ubuntu@192.168.1.10
```

### 24. What is the default SSH port?

22

### 25. How to check open ports?

```bash
netstat -tulnp
```

or

```bash
ss -tulnp
```

---

# 4. Important Linux Commands for DevOps

### 26. How do you search for a file?

```bash
find / -name file.txt
```

### 27. What is grep?

grep searches for patterns inside files.

Example:

```bash
grep "error" log.txt
```

### 28. What is tar command?

Used to compress and archive files.

Create archive:

```bash
tar -cvf file.tar folder
```

Extract archive:

```bash
tar -xvf file.tar
```

### 29. What is cron?

cron is used to schedule tasks in Linux.

Edit cron jobs:

```bash
crontab -e
```

Example job:

```
0 2 * * * backup.sh
```

Runs every day at 2 AM.

### 30. Where are logs stored in Linux?

Most logs are stored in:

```
/var/log
```

Examples:

```
/var/log/syslog
/var/log/messages
```

---

# 5. DevOps Linux Questions

### 31. How do you check running services?

```bash
systemctl status nginx
```

### 32. How do you start a service?

```bash
systemctl start nginx
```

### 33. How do you enable a service at boot?

```bash
systemctl enable nginx
```

### 34. What is systemd?

systemd is the service manager in modern Linux systems.  
It manages services, boot processes, and system processes.

### 35. Difference between apt and yum

apt  
Used in Ubuntu/Debian systems

yum  
Used in RedHat/CentOS systems

### 36. How do you check disk usage?

```bash
df -h
```

### 37. How do you check large files?

```bash
du -ah | sort -rh | head -10
```

### 38. What happens if disk is full?

Possible solutions:
- Remove unnecessary files
- Clean logs
- Extend disk
- Delete old backups

### 39. How do you monitor logs in real time?

```bash
tail -f /var/log/syslog
```

### 40. How do you check system uptime?

```bash
uptime
```

---

# ⭐ Important Linux Commands for DevOps

```
ls
cd
pwd
cp
mv
rm
cat
nano
vim
top
ps
df
du
chmod
chown
grep
find
tar
ssh
scp
crontab
systemctl
```

---

# 🚀 DevOps Note

Linux is the foundation of most DevOps tools such as:

- Docker
- Kubernetes
- Jenkins
- Terraform
- AWS
- CI/CD pipelines

Strong Linux knowledge is essential for DevOps engineers.
