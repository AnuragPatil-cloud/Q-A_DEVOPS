# 🐚 Bash Interview Questions & Answers (DevOps)

This section covers commonly asked **Bash / Shell Scripting interview questions** for DevOps engineers.

---

# 1. What is Bash?

Bash stands for **Bourne Again Shell**.  
It is a **command-line interpreter** used to interact with the Linux operating system and execute commands or scripts.

---

# 2. What is a Bash script?

A Bash script is a **file containing a sequence of Linux commands** that are executed automatically.

Example:

```bash
#!/bin/bash
echo "Hello DevOps"
```

Run the script:

```bash
chmod +x script.sh
./script.sh
```

---

# 3. What is Shebang in Bash?

The first line of a script that tells the system which interpreter to use.

Example:

```bash
#!/bin/bash
```

---

# 4. How do you declare variables in Bash?

Example:

```bash
name="Anurag"
echo $name
```

Note: No space is allowed around `=`.

---

# 5. Difference between $var and ${var}

Both are used to access variables.

Example:

```bash
name="DevOps"

echo $name
echo ${name}
```

`${var}` is useful when combining variables with text.

Example:

```bash
echo "${name}_engineer"
```

---

# 6. What are positional parameters?

Positional parameters represent arguments passed to a script.

Example:

```bash
#!/bin/bash
echo $1
echo $2
```

Run:

```bash
./script.sh hello world
```

Output:

```
hello
world
```

---

# 7. What is $0 in Bash?

`$0` represents the **script name**.

Example:

```bash
echo $0
```

---

# 8. What is $#, $@ and $? in Bash?

| Variable | Meaning |
|--------|--------|
| `$#` | Number of arguments |
| `$@` | All arguments |
| `$?` | Exit status of last command |

Example:

```bash
echo $#
echo $@
echo $?
```

---

# 9. What are conditional statements in Bash?

Conditional statements allow scripts to make decisions.

Example:

```bash
#!/bin/bash

num=10

if [ $num -gt 5 ]
then
echo "Number is greater than 5"
fi
```

---

# 10. What are loops in Bash?

Loops are used to execute commands repeatedly.

Types:
- for loop
- while loop
- until loop

Example (for loop):

```bash
for i in 1 2 3
do
echo $i
done
```

---

# 11. Example of while loop

```bash
count=1

while [ $count -le 5 ]
do
echo $count
((count++))
done
```

---

# 12. What is a function in Bash?

Functions help reuse code.

Example:

```bash
function greet() {
echo "Hello DevOps Engineer"
}

greet
```

---

# 13. How do you take user input in Bash?

Example:

```bash
read name
echo "Hello $name"
```

---

# 14. How to check if a file exists?

Example:

```bash
if [ -f file.txt ]
then
echo "File exists"
else
echo "File not found"
fi
```

---

# 15. How to check if a directory exists?

```bash
if [ -d folder ]
then
echo "Directory exists"
fi
```

---

# 16. What are comparison operators?

Numeric operators:

| Operator | Meaning |
|--------|--------|
| -eq | equal |
| -ne | not equal |
| -gt | greater than |
| -lt | less than |
| -ge | greater or equal |
| -le | less or equal |

Example:

```bash
if [ $a -gt $b ]
then
echo "A is greater"
fi
```

---

# 17. What are logical operators?

| Operator | Meaning |
|--------|--------|
| && | AND |
| || | OR |
| ! | NOT |

Example:

```bash
if [ $a -gt 5 ] && [ $a -lt 20 ]
then
echo "Valid number"
fi
```

---

# 18. How do you debug a Bash script?

Use:

```bash
bash -x script.sh
```

This prints each command as it executes.

---

# 19. What is cron in Linux?

Cron is used to **schedule scripts automatically**.

Example:

```bash
crontab -e
```

Example cron job:

```
0 3 * * * /home/backup.sh
```

Runs every day at **3 AM**.

---

# 20. Example DevOps Bash Script (Disk Monitoring)

```bash
#!/bin/bash

usage=$(df / | grep / | awk '{print $5}' | sed 's/%//')

if [ $usage -gt 80 ]
then
echo "Disk usage is above 80%"
else
echo "Disk usage is normal"
fi
```

---

# 🚀 Why Bash is Important for DevOps

Bash scripting is used for:

- Automation
- CI/CD pipelines
- Server management
- Log monitoring
- Backup scripts
- Infrastructure automation

DevOps engineers frequently use Bash with:

- Linux
- Docker
- Kubernetes
- Jenkins
- Terraform
- AWS

---

# ⭐ Common Bash Commands

```
echo
read
chmod
chown
grep
awk
sed
cut
find
tar
crontab
```

---

# 💡 DevOps Tip

Most **DevOps automation scripts** are written in **Bash or Python**, especially for:

- Server automation
- Deployment scripts
- Log monitoring
- Backup automation
