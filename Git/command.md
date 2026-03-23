# 🔧 Git Commands for DevOps (2+ Years Experience)

This section covers **advanced Git commands with explanations** commonly used by DevOps engineers in real projects.

---

# 📌 1. Git Clone (with depth)

Clone repository with limited history (faster for CI/CD):

```
git clone --depth=1 <repo-url>
```

👉 Used in pipelines to reduce clone time.

---

# 📌 2. Git Branch Management

List branches:

```
git branch
```

Create new branch:

```
git checkout -b feature-branch
```

Delete branch:

```
git branch -d feature-branch
```

👉 Used in feature-based development.

---

# 📌 3. Git Fetch vs Pull

Fetch latest changes (without merge):

```
git fetch origin
```

Pull changes (fetch + merge):

```
git pull origin main
```

👉 DevOps best practice: use **fetch before merge**.

---

# 📌 4. Git Rebase (Clean History)

```
git rebase main
```

👉 Moves your commits on top of main branch  
👉 Used to maintain **clean commit history**

---

# 📌 5. Git Merge

```
git merge feature-branch
```

👉 Combines branches  
👉 Keeps history intact

---

# 📌 6. Git Stash (Temporary Save)

Save uncommitted changes:

```
git stash
```

Apply stash:

```
git stash apply
```

List stashes:

```
git stash list
```

👉 Useful during **hotfix or branch switching**

---

# 📌 7. Git Reset

Soft reset (keep changes):

```
git reset --soft HEAD~1
```

Hard reset (delete changes):

```
git reset --hard HEAD~1
```

👉 Used to undo commits

---

# 📌 8. Git Revert (Safe Undo)

```
git revert <commit-id>
```

👉 Creates new commit to undo changes  
👉 Safe for **production**

---

# 📌 9. Git Log (Advanced)

```
git log --oneline --graph --all
```

👉 Visualize commit history

---

# 📌 10. Git Diff

```
git diff
```

👉 Shows changes between files/commits

---

# 📌 11. Git Cherry-Pick

```
git cherry-pick <commit-id>
```

👉 Apply specific commit to another branch

---

# 📌 12. Git Tag (Releases)

Create tag:

```
git tag v1.0
```

Push tag:

```
git push origin v1.0
```

👉 Used in release management

---

# 📌 13. Git Remote

Check remote:

```
git remote -v
```

Add remote:

```
git remote add origin <url>
```

---

# 📌 14. Git Clean

Remove untracked files:

```
git clean -fd
```

👉 Useful in CI/CD pipelines

---

# 📌 15. Git Reflog (Recovery)

```
git reflog
```

👉 Recover deleted commits

---

# 📌 16. Git Blame

```
git blame file.txt
```

👉 Shows who changed each line

---

# 📌 17. Git Show

```
git show <commit-id>
```

👉 View commit details

---

# 📌 18. Git Squash (Interactive Rebase)

```
git rebase -i HEAD~3
```

👉 Combine commits into one

---

# 📌 19. Git Force Push (Safe Way)

```
git push --force-with-lease
```

👉 Prevents overwriting others’ work

---

# 📌 20. Git Submodule

```
git submodule add <repo-url>
```

👉 Used to manage external dependencies

---

# 🚀 DevOps Real Usage Examples

## CI/CD Pipeline Clone Optimization
```
git clone --depth=1
```

## Fix Production Bug
```
git revert <commit-id>
```

## Apply Hotfix to Another Branch
```
git cherry-pick <commit-id>
```

## Clean Workspace
```
git clean -fd
```

---

# 🎯 Why These Commands Are Important

DevOps engineers use Git for:

- CI/CD pipelines
- version control
- release management
- debugging production issues
- collaboration

Mastering these commands shows **real-world DevOps experience**.
