# 🐧 Linux Commands Cheat Sheet (DevOps)

This section contains commonly used **Linux commands for DevOps engineers** (Interview + Practical).

---

# 📂 File & Directory Commands

```
pwd                 # Show current directory
ls                  # List files
ls -l               # Detailed list
ls -a               # Show hidden files
cd <dir>            # Change directory
cd ..               # Go back one directory
mkdir <dir>         # Create directory
rmdir <dir>         # Remove empty directory
rm -rf <dir/file>   # Delete file or directory
cp file1 file2      # Copy file
mv file1 file2      # Move/rename file
touch file.txt      # Create file
```

---

# 📄 File Viewing Commands

```
cat file.txt        # View file content
less file.txt       # View file page by page
head -n 10 file.txt # First 10 lines
tail -n 10 file.txt # Last 10 lines
tail -f file.txt    # Live log monitoring
```

---

# 🔍 Search & Filter Commands

```
grep "text" file.txt         # Search text
grep -i "text" file.txt      # Case insensitive
find / -name file.txt        # Find file
locate file.txt              # Locate file quickly
which python                 # Show command path
```

---

# ⚙️ Permissions & Ownership

```
chmod 755 file.sh            # Change permissions
chmod +x file.sh             # Make executable
chown user:group file        # Change ownership
ls -l                        # Check permissions
```

---

# 👤 User Management

```
useradd user1                # Create user
passwd user1                 # Set password
usermod -aG sudo user1       # Add to group
id user1                     # Show user info
whoami                       # Current user
```

---

# 💾 Disk & Memory

```
df -h                        # Disk usage
du -sh folder/               # Folder size
free -m                      # Memory usage
top                          # Real-time processes
htop                         # Enhanced top
```

---

# 📦 Package Management (Ubuntu)

```
apt update                   # Update packages
apt upgrade                  # Upgrade packages
apt install nginx            # Install package
apt remove nginx             # Remove package
```

---

# 🌐 Networking Commands

```
ip a                         # Show IP address
ping google.com              # Check connectivity
netstat -tulnp               # Open ports
ss -tulnp                    # Alternative to netstat
curl http://example.com      # Fetch URL
wget http://example.com      # Download file
```

---

# 🔄 Process Management

```
ps aux                       # List processes
kill <pid>                   # Kill process
kill -9 <pid>                # Force kill
pkill nginx                  # Kill by name
systemctl start nginx        # Start service
systemctl stop nginx         # Stop service
systemctl status nginx       # Service status
systemctl enable nginx       # Enable on boot
```

---

# 📦 Archive & Compression

```
tar -cvf file.tar dir/       # Create tar
tar -xvf file.tar            # Extract tar
tar -czvf file.tar.gz dir/   # Compress
tar -xzvf file.tar.gz        # Extract gzip
zip file.zip file.txt        # Create zip
unzip file.zip               # Extract zip
```

---

# 📜 Logs & Monitoring

```
tail -f /var/log/syslog      # Monitor logs
dmesg                        # Kernel logs
journalctl -u nginx          # Service logs
```

---

# 🔧 System Information

```
uname -a                     # System info
uptime                       # System uptime
hostname                     # Hostname
who                          # Logged-in users
```

---

# 🚀 DevOps Important Commands

```
history                      # Command history
alias ll='ls -l'             # Create shortcut
crontab -e                   # Schedule jobs
watch df -h                  # Monitor command output
```

---

# 🎯 Why Linux Commands Are Important for DevOps

DevOps engineers use Linux commands to:

- manage servers
- troubleshoot issues
- monitor systems
- automate tasks
- deploy applications
