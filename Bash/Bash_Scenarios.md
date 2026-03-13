# 🐚 Bash Scripting Scenario-Based DevOps Interview Questions

This section contains **real-world Bash scripting scenarios** commonly faced by DevOps engineers.

---

# Scenario 1: Script Not Executing

### Problem
A Bash script does not run when executed.

### Possible Causes

- execute permission missing
- incorrect shebang line
- syntax errors in script

### Solution

Give execute permission:

```
chmod +x script.sh
```

Verify shebang:

```
#!/bin/bash
```

Run script using:

```
bash script.sh
```

---

# Scenario 2: Disk Space Monitoring Script

### Problem
You need to monitor disk usage and alert if disk usage exceeds 80%.

### Solution

Example Bash script:

```
#!/bin/bash

usage=$(df / | grep / | awk '{print $5}' | sed 's/%//')

if [ $usage -gt 80 ]
then
 echo "Disk usage above 80%"
else
 echo "Disk usage normal"
fi
```

---

# Scenario 3: Automated Backup Script

### Problem
You need to create daily backups of a directory.

### Solution

Example script:

```
#!/bin/bash

tar -czf backup_$(date +%F).tar.gz /home/user/data
```

Schedule using cron:

```
0 2 * * * /backup.sh
```

---

# Scenario 4: Process Monitoring Script

### Problem
Check if a specific service is running and restart it if stopped.

### Solution

Example script:

```
#!/bin/bash

service=nginx

if pgrep $service > /dev/null
then
 echo "Service running"
else
 echo "Service stopped, restarting..."
 systemctl start nginx
fi
```

---

# Scenario 5: Log File Cleanup Script

### Problem
Server logs are consuming too much disk space.

### Solution

Delete logs older than 7 days:

```
find /var/log -type f -mtime +7 -delete
```

Automate with cron.

---

# Scenario 6: Script Fails Due to Permission Error

### Problem
Script fails with:

```
Permission denied
```

### Cause

Script lacks proper permissions.

### Solution

Give correct permissions:

```
chmod 755 script.sh
```

---

# Scenario 7: Script Needs to Run Automatically

### Problem
Script should run automatically every day.

### Solution

Use **cron job**.

Edit cron:

```
crontab -e
```

Example:

```
0 3 * * * /scripts/backup.sh
```

This runs script at **3 AM daily**.

---

# Scenario 8: Script Not Receiving Input Arguments

### Problem
Script expects arguments but fails.

### Solution

Use positional parameters.

Example:

```
#!/bin/bash

echo "First argument: $1"
echo "Second argument: $2"
```

Run script:

```
./script.sh hello world
```

---

# Scenario 9: Need to Monitor Server Load

### Problem
DevOps team needs to monitor CPU load.

### Solution

Use:

```
top
```

or

```
uptime
```

Example script:

```
#!/bin/bash
uptime
```

---

# Scenario 10: Multiple Servers Need Same Script

### Problem
Same script must run on multiple servers.

### Solution

Use:

- Ansible
- SSH automation
- CI/CD pipelines

This helps automate script execution across servers.

---

# 🎯 Why Bash Scenarios Are Important for DevOps

DevOps engineers frequently use Bash scripting to automate:

- system monitoring
- backups
- deployment scripts
- log cleanup
- server maintenance

Understanding these scenarios helps maintain **efficient and automated infrastructure management**.
