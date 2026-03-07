# 🔧 Git Interview Questions & Answers (DevOps)

This section contains commonly asked **Git interview questions for DevOps Engineers (Fresher – 2 Years Experience).**

---

# 1. What is Git?

Git is a **distributed version control system** used to track changes in source code during software development.

It allows multiple developers to work on the same project without overwriting each other's changes.

---

# 2. What is Version Control?

Version control is a system that **tracks changes to files over time** so that you can recall specific versions later.

Example tools:
- Git
- SVN
- Mercurial

---

# 3. What is the difference between Git and GitHub?

Git  
- Version control system  
- Installed locally on your system  

GitHub  
- Cloud platform that hosts Git repositories  
- Used for collaboration

---

# 4. What is a Git repository?

A Git repository is a **directory where Git tracks all files and their version history**.

Initialize a repository:

```bash
git init
```

---

# 5. What is the Git workflow?

Basic Git workflow:

Working Directory  
↓  
Staging Area  
↓  
Local Repository  
↓  
Remote Repository

---

# 6. What is the staging area?

The staging area is where you **prepare files before committing them to the repository**.

Example:

```bash
git add file.txt
```

---

# 7. What is a commit?

A commit saves changes to the local repository.

Example:

```bash
git commit -m "Added login feature"
```

---

# 8. What does `git clone` do?

It creates a copy of a remote repository on your local system.

Example:

```bash
git clone https://github.com/user/repository.git
```

---

# 9. What is `git pull`?

`git pull` downloads changes from a remote repository and merges them into the current branch.

```bash
git pull origin main
```

---

# 10. What is `git push`?

`git push` uploads local commits to the remote repository.

```bash
git push origin main
```

---

# 11. What is a branch in Git?

A branch is a **separate line of development** used to work on new features without affecting the main code.

Create a branch:

```bash
git branch feature
```

---

# 12. How do you switch branches?

```bash
git checkout branch-name
```

or

```bash
git switch branch-name
```

---

# 13. How do you create and switch to a branch?

```bash
git checkout -b feature
```

---

# 14. What is Git merge?

Merge combines changes from one branch into another.

Example:

```bash
git merge feature
```

---

# 15. What is a merge conflict?

A merge conflict occurs when **two branches modify the same part of a file** and Git cannot automatically merge them.

You must resolve the conflict manually.

---

# 16. What is `git status`?

Shows the current state of the repository.

Example:

```bash
git status
```

---

# 17. What is `git log`?

Displays commit history.

```bash
git log
```

---

# 18. What is `git diff`?

Shows differences between files or commits.

```bash
git diff
```

---

# 19. What is `.gitignore`?

`.gitignore` is used to **exclude files from being tracked by Git**.

Example:

```
node_modules
*.log
.env
```

---

# 20. What is `git stash`?

`git stash` temporarily saves changes without committing them.

Example:

```bash
git stash
```

Restore stash:

```bash
git stash pop
```

---

# 21. What is `git reset`?

Used to undo commits.

Example:

```bash
git reset --soft HEAD~1
```

---

# 22. What is `git revert`?

Creates a new commit that undoes changes from a previous commit.

```bash
git revert commit_id
```

---

# 23. What is `git fetch`?

`git fetch` downloads changes from the remote repository but **does not merge them automatically**.

```bash
git fetch origin
```

---

# 24. Difference between `git pull` and `git fetch`

git fetch  
Downloads changes but does not merge them.

git pull  
Downloads changes and merges them automatically.

---

# 25. What is `git tag`?

Tags are used to mark specific points in history such as releases.

Example:

```bash
git tag v1.0
```

---

# 26. How do you check branches?

```bash
git branch
```

---

# 27. How do you delete a branch?

```bash
git branch -d branch-name
```

---

# 28. How do you see remote repositories?

```bash
git remote -v
```

---

# 29. What is `git rebase`?

Rebase moves commits from one branch onto another to create a cleaner commit history.

Example:

```bash
git rebase main
```

---

# 30. Important Git Commands for DevOps

```
git init
git clone
git status
git add
git commit
git push
git pull
git fetch
git branch
git checkout
git merge
git rebase
git log
git diff
git stash
git reset
git revert
```

---

# 🚀 Why Git is Important for DevOps

Git is used in DevOps for:

- Source code management
- CI/CD pipelines
- Collaboration between teams
- Version control of infrastructure code

Git integrates with tools like:

- GitHub
- GitLab
- Jenkins
- Docker
- Kubernetes
- Terraform
