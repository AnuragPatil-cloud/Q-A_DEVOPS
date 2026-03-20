# 🔧 Git Interview Questions & Answers (DevOps)

This section contains commonly asked **Git interview questions** for DevOps engineers.

---

# 1. What is Git?

Git is a **distributed version control system used to track changes in source code and collaborate with multiple developers**.

It allows teams to manage code efficiently.

---

# 2. What is a Repository in Git?

A repository is a **storage location where project files and version history are maintained**.

Types:

- Local repository
- Remote repository

---

# 3. What is the difference between Git and GitHub?

| Git | GitHub |
|---|---|
Version control system | Cloud-based hosting service |
Works locally | Works remotely |
Tracks changes | Stores repositories |

---

# 4. What is a Commit in Git?

A commit is a **snapshot of changes made to the repository**.

Each commit has:

- unique ID (hash)
- message
- author details

---

# 5. What is a Branch in Git?

A branch is a **separate line of development**.

It allows developers to work on features without affecting the main codebase.

---

# 6. What is the main branch in Git?

The main branch is the **default branch**, usually named:

```
main
```

or

```
master
```

---

# 7. What is Git Merge?

Merge is used to **combine changes from one branch into another**.

Example:

```
git merge feature-branch
```

---

# 8. What is Git Rebase?

Rebase is used to **apply commits from one branch onto another branch**.

It creates a linear commit history.

---

# 9. What is the difference between Merge and Rebase?

| Merge | Rebase |
|---|---|
Keeps history | Rewrites history |
Creates merge commit | No merge commit |
Safer | Cleaner history |

---

# 10. What is Git Clone?

Git clone is used to **copy a remote repository to your local machine**.

Example:

```
git clone <repo-url>
```

---

# 11. What is Git Pull?

Git pull is used to **fetch and merge changes from a remote repository**.

Example:

```
git pull origin main
```

---

# 12. What is Git Push?

Git push is used to **upload local commits to a remote repository**.

Example:

```
git push origin main
```

---

# 13. What is Git Fetch?

Git fetch is used to **download changes from a remote repository without merging them**.

---

# 14. What is Git Staging Area?

The staging area is where **changes are prepared before committing**.

Command:

```
git add .
```

---

# 15. What is .gitignore?

.gitignore is a file used to **exclude certain files or directories from being tracked by Git**.

Example:

```
node_modules/
*.log
```

---

# 16. What is Git Log?

Git log shows the **history of commits in the repository**.

Example:

```
git log
```

---

# 17. What is Git Reset?

Git reset is used to **undo changes or move the HEAD pointer to a previous commit**.

---

# 18. What is Git Revert?

Git revert is used to **undo a commit by creating a new commit**.

It is safer than reset.

---

# 19. What is a Pull Request (PR)?

A pull request is used to **request merging changes from one branch into another in a remote repository**.

It allows code review before merging.

---

# 20. Why is Git important for DevOps?

Git is important because it enables:

- version control
- collaboration
- CI/CD integration
- code tracking and rollback
