# 🐚 Shell Scripting Interview Questions & Answers (DevOps)

This section contains commonly asked **Shell Scripting interview questions for DevOps Engineers (Fresher – 2+ Years Experience).**

---

# 1. What is Shell Scripting?

Shell scripting is the process of **writing a sequence of commands in a file to automate tasks in Linux or Unix systems**.

Shell scripts help automate repetitive tasks such as:

- System monitoring
- Backup
- Deployment
- File management

---

# 2. What is a Shell?

A shell is a **command-line interpreter that allows users to interact with the operating system**.

Examples:

- Bash
- Sh
- Zsh
- Ksh

---

# 3. What is Bash?

Bash stands for **Bourne Again Shell**.

It is the **most commonly used shell in Linux systems**.

---

# 4. What is a Shell Script?

A shell script is a **file containing a list of Linux commands executed sequentially**.

Example:

```bash
#!/bin/bash
echo "Hello DevOps"
```

---

# 5. What is Shebang in Shell Script?

The shebang line tells the system **which interpreter should execute the script**.

Example:

```
#!/bin/bash
```

---

# 6. How do you run a shell script?

Steps:

1. Give execute permission

```
chmod +x script.sh
```

2. Run the script

```
./script.sh
```

---

# 7. How do you declare variables in shell scripting?

Example:

```bash
name="Anurag"
echo $name
```

---

# 8. What are positional parameters?

Positional parameters represent **arguments passed to a script**.

Example script:

```bash
#!/bin/bash
echo $1
echo $2
```

Run script:

```
./script.sh hello world
```

Output:

```
hello
world
```

---

# 9. What are special variables in shell scripting?

Common special variables:

```
$0  → script name
$1  → first argument
$#  → number of arguments
$@  → all arguments
$?  → exit status
$$  → process ID
```

---

# 10. What are conditional statements in shell scripting?

Conditional statements allow scripts to make decisions.

Example:

```bash
if [ $a -gt $b ]
then
echo "A is greater"
fi
```

---

# 11. What are loops in shell scripting?

Loops execute commands repeatedly.

Types of loops:

- for loop
- while loop
- until loop

Example for loop:

```bash
for i in 1 2 3
do
echo $i
done
```

---

# 12. Example of while loop

```bash
count=1

while [ $count -le 5 ]
do
echo $count
((count++))
done
```

---

# 13. What are functions in shell scripting?

Functions allow **reusing code multiple times**.

Example:

```bash
function greet() {
echo "Hello DevOps"
}

greet
```

---

# 14. How do you take user input in shell scripting?

Example:

```bash
read name
echo "Hello $name"
```

---

# 15. How do you check if a file exists?

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

# 16. What are comparison operators?

Numeric comparison operators:

```
-eq → equal
-ne → not equal
-gt → greater than
-lt → less than
-ge → greater or equal
-le → less or equal
```

---

# 17. What are logical operators?

Logical operators used in shell scripting:

```
&& → AND
|| → OR
!  → NOT
```

---

# 18. How do you debug a shell script?

Use the `-x` option:

```
bash -x script.sh
```

This prints each command as it executes.

---

# 19. Real DevOps Shell Script Example

Example: Check disk usage

```bash
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

# 20. Why Shell Scripting is Important for DevOps

Shell scripting helps DevOps engineers:

- Automate system tasks
- Manage servers
- Write deployment scripts
- Monitor infrastructure
- Automate CI/CD pipelines

Shell scripting is widely used with:

- Linux
- Docker
- Kubernetes
- Jenkins
- Cloud environments
