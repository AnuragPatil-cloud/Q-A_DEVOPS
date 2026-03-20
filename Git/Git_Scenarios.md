# 🔧 Git Scenario-Based DevOps Interview Questions

This section contains **real-world Git troubleshooting scenarios** commonly faced by DevOps engineers.

---

# Scenario 1: Merge Conflict During Git Pull

### Problem
While pulling code, you get a **merge conflict**.

### Cause

Same file modified in multiple branches.

### Solution

Check conflicted files:

```
git status
```

Open file and resolve conflicts manually:

```
<<<<<<< HEAD
Your changes
=======
Incoming changes
>>>>>>> branch
```

After resolving:

```
git add .
git commit -m "resolved conflict"
```

---

# Scenario 2: Accidentally Committed Wrong Code

### Problem
You committed incorrect changes.

### Solution

Undo last commit (keep changes):

```
git reset --soft HEAD~1
```

Undo last commit (remove changes):

```
git reset --hard HEAD~1
```

---

# Scenario 3: Changes Not Reflecting After Pull

### Problem
You pulled latest code but changes are not visible.

### Possible Causes

- wrong branch
- local changes not committed

### Solution

Check branch:

```
git branch
```

Switch branch if needed:

```
git checkout main
```

---

# Scenario 4: Need to Undo a Commit in Production

### Problem
A bad commit is already pushed to remote.

### Solution

Use revert:

```
git revert <commit-id>
```

This creates a new commit that undoes changes safely.

---

# Scenario 5: Branch Not Updating

### Problem
Your branch is behind remote.

### Solution

Fetch latest changes:

```
git fetch origin
```

Merge:

```
git merge origin/main
```

---

# Scenario 6: Force Push Issue

### Problem
Force push overwrites remote history.

### Risk

Other developers may lose their work.

### Solution

Use safely:

```
git push --force-with-lease
```

---

# Scenario 7: Lost Changes After Reset

### Problem
You accidentally used `git reset --hard`.

### Solution

Recover using:

```
git reflog
```

Then restore commit:

```
git checkout <commit-id>
```

---

# Scenario 8: Large Files Accidentally Added

### Problem
Large files committed to repository.

### Solution

Remove file:

```
git rm --cached <file>
```

Add to `.gitignore`.

---

# Scenario 9: Need to Create New Branch from Existing Code

### Problem
You need to work on a new feature.

### Solution

Create branch:

```
git checkout -b feature-branch
```

Push branch:

```
git push origin feature-branch
```

---

# Scenario 10: Multiple Developers Working on Same Code

### Problem
Code conflicts and version issues.

### Solution

Follow best practices:

- use feature branches
- pull latest code before pushing
- create pull requests
- perform code reviews

---

# 🎯 Why Git Scenarios Are Important for DevOps

DevOps engineers must handle:

- merge conflicts
- code rollbacks
- collaboration issues
- version control problems

Understanding these scenarios helps maintain **smooth CI/CD workflows and team collaboration**.
