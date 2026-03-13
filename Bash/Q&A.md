# 🐚 Bash Scripting Interview Questions & Answers (DevOps)

This section contains commonly asked **Bash scripting interview questions** for DevOps engineers.

---

# 1. What is Bash?

Bash (Bourne Again Shell) is a **command-line interpreter used in Linux systems to execute commands and scripts**.

It allows users to interact with the operating system.

---

# 2. What is Bash scripting?

Bash scripting is the process of **writing a sequence of commands in a script file to automate tasks in Linux systems**.

Example uses:

- server automation
- log management
- deployment scripts
- monitoring tasks

---

# 3. What is a Shebang in Bash?

The shebang line specifies **which interpreter should execute the script**.

Example:

```
#!/bin/bash
```

This tells the system to execute the script using Bash.

---

# 4. How do you run a Bash script?

Steps:

Give execute permission:

```
chmod +x script.sh
```

Run the script:

```
./script.sh
```

---

# 5. How do you define variables in Bash?

Variables are defined without spaces.

Example:

```
name="DevOps"
echo $name
```

---

# 6. What are positional parameters in Bash?

Positional parameters represent **arguments passed to a script**.

Example:

```
$1 → first argument
$2 → second argument
$# → number of arguments
$@ → all arguments
```

---

# 7. What are conditional statements in Bash?

Conditional statements allow scripts to make decisions.

Example:

```
if [ $a -gt $b ]
then
 echo "A is greater"
fi
```

---

# 8. What are loops in Bash?

Loops allow executing commands repeatedly.

Types of loops:

- for loop
- while loop
- until loop

Example:

```
for i in 1 2 3
do
 echo $i
done
```

---

# 9. What are functions in Bash?

Functions allow **reusable blocks of code**.

Example:

```
greet() {
 echo "Hello DevOps"
}

greet
```

---

# 10. How do you read user input in Bash?

Example:

```
read name
echo "Hello $name"
```

---

# 11. What are comparison operators in Bash?

Common numeric comparison operators:

```
-eq  equal
-ne  not equal
-gt  greater than
-lt  less than
-ge  greater or equal
-le  less or equal
```

---

# 12. What are logical operators in Bash?

Logical operators include:

```
&&  AND
||  OR
!   NOT
```

---

# 13. How do you check if a file exists in Bash?

Example:

```
if [ -f file.txt ]
then
 echo "File exists"
fi
```

---

# 14. What is the difference between `command` and `shell` module in Bash scripting?

In shell scripts:

- `command` executes commands directly
- `shell` allows complex shell operations like pipes and redirects

Example:

```
ls | grep file
```

---

# 15. What is debugging in Bash?

Debugging helps identify issues in scripts.

Use:

```
bash -x script.sh
```

This prints each command as it executes.

---

# 16. What are environment variables?

Environment variables store system-wide configuration values.

Example:

```
$PATH
$HOME
$USER
```

---

# 17. What is exit status in Bash?

Every command returns an exit status.

```
0 → success
1 → failure
```

Check exit status using:

```
echo $?
```

---

# 18. What is a cron job in Linux?

Cron is used to **schedule tasks to run automatically at specific times**.

Example:

```
0 2 * * * /script.sh
```

This runs the script at **2 AM daily**.

---

# 19. What are common Bash scripting use cases in DevOps?

DevOps engineers use Bash scripting for:

- server automation
- deployment scripts
- monitoring tasks
- log cleanup
- backup scripts

---

# 20. Why is Bash scripting important for DevOps?

Bash scripting helps DevOps teams:

- automate repetitive tasks
- manage servers efficiently
- reduce manual work
- improve operational efficiency
