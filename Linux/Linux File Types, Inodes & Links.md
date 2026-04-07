# 📁 Linux File Types, Inodes & Links – DevOps Interview Guide

---

# 🧠 1. Linux File Types

In Linux, **everything is treated as a file**, including devices and processes.

---

## 📂 Types of Files in Linux

| Symbol | File Type        | Description                   |
| ------ | ---------------- | ----------------------------- |
| `-`    | Regular File     | Text files, scripts, binaries |
| `d`    | Directory        | Folder containing files       |
| `l`    | Symbolic Link    | Shortcut to another file      |
| `c`    | Character Device | Keyboard, terminal            |
| `b`    | Block Device     | Hard disks (e.g., `/dev/sda`) |
| `p`    | Named Pipe       | Inter-process communication   |
| `s`    | Socket           | Network communication         |

---

## 🔍 How to Identify File Types

```bash
ls -l
```

👉 Example Output:

```
-rw-r--r--  file.txt
drwxr-xr-x  mydir
lrwxrwxrwx  link -> file.txt
```

---

# 🔢 2. What is an Inode?

An **inode (index node)** is a data structure that stores metadata about a file.

---

## 📌 Inode Contains:

* File size
* Ownership (user/group)
* Permissions
* Timestamps
* Pointers to data blocks

❌ Does NOT store:

* File name
* File content

---

## 🔍 Check Inode Number

```bash
ls -i file.txt
```

---

## 🧠 Important Concept

👉 Multiple filenames can point to the same inode (Hard Links)

---

# 🔗 3. Hard Link vs Symbolic Link

---

## ⚔️ Difference Table

| Feature          | Hard Link    | Symbolic Link    |
| ---------------- | ------------ | ---------------- |
| Inode            | Same inode   | Different inode  |
| File Type        | Regular file | Special file (l) |
| Cross Filesystem | ❌ No         | ✅ Yes            |
| Delete Original  | Still works  | Broken link      |
| Command          | `ln`         | `ln -s`          |

---

## 🧪 Create Links

### Hard Link

```bash
ln file.txt hardlink.txt
```

### Symbolic Link

```bash
ln -s file.txt symlink.txt
```

---

## 🔍 Verify Links

```bash
ls -li
```

👉 Same inode → Hard link
👉 Different inode → Symlink

---

# 🚀 DevOps Practical Usage

---

## 📌 Where You’ll Use This:

* Log rotation (inodes matter)
* Shared configs using links
* Disk troubleshooting (inode full issue)
* Docker volumes & mounts

---

## 🔥 Real Scenario

👉 Disk is not full but still can't create files

**Reason:**
👉 Inodes exhausted

---

## 🔍 Check Inodes Usage

```bash
df -i
```

---

# 🔥 Interview Questions & Answers

---

## ❓ 1. What are file types in Linux?

**Answer:**
Linux supports multiple file types such as regular files, directories, symbolic links, block devices, character devices, pipes, and sockets.

---

## ❓ 2. What is an inode?

**Answer:**
An inode is a metadata structure that stores information about a file except its name and actual data.

---

## ❓ 3. What information is stored in an inode?

**Answer:**

* Permissions
* Owner
* File size
* Timestamps
* Disk block pointers

---

## ❓ 4. How do you check inode number?

```bash
ls -i filename
```

---

## ❓ 5. What happens when inode limit is reached?

**Answer:**
No new files can be created even if disk space is available.

---

## ❓ 6. Difference between Hard Link and Symbolic Link?

**Answer:**

* Hard link shares same inode
* Symbolic link points to original file path

---

## ❓ 7. Can hard links cross filesystems?

**Answer:**
❌ No, hard links cannot cross filesystems.

---

## ❓ 8. What happens if original file is deleted?

**Answer:**

* Hard link → still works
* Symbolic link → broken

---

## ❓ 9. How to find all links of a file?

```bash
ls -li
```

---

## ❓ 10. Why are symbolic links used?

**Answer:**
To create shortcuts, manage shared configurations, and link files across directories/filesystems.

---

# ⚙️ Important Commands

```bash
ls -l        # file types
ls -i        # inode number
df -i        # inode usage
ln           # create hard link
ln -s        # create symbolic link
stat file    # detailed inode info
```

---

# 🎯 Pro Tips for DevOps Interview

* Always explain with **real scenarios**
* Mention **inode full issue** (very common question)
* Show difference using `ls -li`
* Use examples of **logs, configs, docker volumes**

---

# ✅ One-Line Summary

👉 *Linux uses inodes to manage file metadata, and links (hard & symbolic) provide flexible ways to reference files across the system.*

---

# ⭐ Use This Repo For

* DevOps Interview Preparation
* Linux Fundamentals
* Troubleshooting Practice

---

🔥 **Pro Tip:** Practice by creating files, links, and checking inodes in real Linux systems.

---
