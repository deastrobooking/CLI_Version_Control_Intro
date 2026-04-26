
# Setup Git

## 1. Verify Installation

```bash
git --version
git config --list
```

## 2. Configure User Info (Required)

```bash
git config --global user.name "Your Name"
git config --global user.email your@email.com
```

Verify:

```bash
git config user.name
git config user.email
```

---

# Git Basics

## Git has 3 states:

* **Working Directory** → where you edit files
* **Staging Area** → files prepared for commit
* **Repository (.git)** → committed snapshots

---

# Project: Project Monkey

## 1. Create Project Folder

```bash
mkdir projectmonkey
cd projectmonkey
```

## 2. Initialize Repository

```bash
git init
```

## 3. View Hidden Files

```bash
ls -la   # Mac/Linux
```

---

# Create First File

Create:

```bash
HelloMonkey.java
```

```java
public class HelloMonkey {
    public static void main(String[] args) {
        System.out.println("Welcome to Project Monkey");
    }
}
```

---

# Git Workflow

## 1. Check Status

```bash
git status
```

## 2. Stage File

```bash
git add HelloMonkey.java
```

## 3. Commit File

```bash
git commit -m "Initial Project Monkey Commit"
```

## 4. Verify

```bash
git status
```

---

# Modify & Add Files

## Create README

```bash
README.txt
```

Add:

```
Information about Project Monkey will go in this file.
```

## Modify Java File

Add comment:

```java
// This is the main file for Project Monkey
```

---

## Stage & Commit Changes

```bash
git add --all
git commit -m "Added README and updated HelloMonkey"
```

---

# View History

```bash
git log
```

Short version:

```bash
git log --pretty=oneline
```

---

# Remove File from Staging

```bash
git rm --cached junk.txt
```

---

# Branching & Merging

## Create New Repo

```bash
cd ..
git init websites
cd websites
```

---


---

## Track and Commit

```bash
git add index.html
git commit -m "Initial website commit"
```

---

## Create Branch

```bash
git branch feature1.0
git checkout feature1.0
```

---

## Make Changes (Feature Branch)

Add:

* Contact info
* Under construction message

Then:

```bash
git add index.html
git commit -m "Feature 1.0 updates"
```

---

## Switch Back to Master

```bash
git checkout master
```

Make different changes (ex: background color)

```bash
git add index.html
git commit -m "Updated master version"
```

---

## Merge Feature Branch

```bash
git merge feature1.0
```

---

# Git History & Navigation

View logs:

```bash
git log
```

View last commit:

```bash
git log -1
```

Checkout old version:

```bash
git checkout <commit-hash>
```

---

# GitHub Section

## 1. Create Repo on GitHub

* Name: `myfirstrepo`
* Public
* Initialize with README

---

## 2. Clone Repo

```bash
git clone <repo-url>
cd myfirstrepo
```

---

## 3. Modify README

Add:

```
Hello from my PC!
```

---

## 4. Commit & Push

```bash
git add .
git commit -m "Updated README from local"
git push <repo-url>
```

---

# Final Deliverable

* Take a screenshot of your **GitHub commit history**
* Upload to assignment dropbox

---

# Key Commands Summary

```bash
git init
git status
git add
git commit
git log
git branch
git checkout
git merge
git clone
git push
```

---

