# 🐧 Linux Scenario-Based DevOps Interview Questions

This section contains **real-world Linux troubleshooting scenarios** commonly faced by DevOps engineers.

---

# Scenario 1: Server Not Reachable

### Problem
Unable to SSH into server.

### Possible Causes

- server down
- network issue
- firewall blocking SSH
- wrong IP

### Solution

Check:

```
ping <server-ip>
```

Verify SSH service:

```
systemctl status sshd
```

Check firewall:

```
iptables -L
```

---

# Scenario 2: Disk Space Full

### Problem
Server shows:

```
No space left on device
```

### Solution

Check disk usage:

```
df -h
```

Find large files:

```
du -sh /*
```

Clean logs:

```
rm -rf /var/log/*.log
```

---

# Scenario 3: High CPU Usage

### Problem
Server performance is slow.

### Solution

Check processes:

```
top
```

or

```
ps aux --sort=-%cpu
```

Kill process:

```
kill -9 <pid>
```

---

# Scenario 4: Service Not Starting

### Problem
Service (e.g., nginx) not starting.

### Solution

Check status:

```
systemctl status nginx
```

Check logs:

```
journalctl -u nginx
```

Fix configuration and restart.

---

# Scenario 5: Permission Denied Error

### Problem
File access error:

```
Permission denied
```

### Solution

Check permissions:

```
ls -l
```

Fix permissions:

```
chmod 755 file
chown user:user file
```

---

# Scenario 6: Port Already in Use

### Problem
Application fails to start due to port conflict.

### Solution

Check port:

```
netstat -tulnp | grep 8080
```

Kill process:

```
kill -9 <pid>
```

---

# Scenario 7: Application Not Accessible

### Problem
Application running but not accessible.

### Possible Causes

- firewall blocking port
- service not listening
- network issue

### Solution

Check:

```
ss -tulnp
```

Allow port:

```
ufw allow 80
```

---

# Scenario 8: Cron Job Not Running

### Problem
Scheduled job not executing.

### Solution

Check cron service:

```
systemctl status cron
```

Verify cron job:

```
crontab -l
```

Check logs:

```
/var/log/syslog
```

---

# Scenario 9: File Not Found Error

### Problem
Script cannot find file.

### Cause

Wrong path or file missing.

### Solution

Check file:

```
ls -l /path/to/file
```

Use absolute path.

---

# Scenario 10: Memory Usage High

### Problem
Server memory is almost full.

### Solution

Check memory:

```
free -m
```

Check processes:

```
ps aux --sort=-%mem
```

Restart services if needed.

---

# 🎯 Why Linux Scenarios Are Important for DevOps

DevOps engineers must troubleshoot:

- server issues
- resource utilization
- service failures
- network problems
- permissions

Understanding these scenarios helps maintain **stable and reliable infrastructure**.
