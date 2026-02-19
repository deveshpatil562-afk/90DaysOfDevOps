# Day 25 – Git Reset vs Revert & Branching Strategies

Repository: devops-git-practice  
File: day-25-notes.md  

---

# 📌 Overview

Today I learned how to safely undo mistakes in Git using:

- [git reset]
- [git revert]

I also explored real-world branching strategies used by engineering teams to manage code efficiently at scale.

This is one of the most important Git concepts because mistakes are inevitable — handling them safely is what makes a strong DevOps engineer.

---

# ✅ Task 1: Git Reset — Hands-On

## 🔹 Step 1: Create 3 Commits

[echo "Commit A" > file.txt]  
[git add file.txt]  
[git commit -m "commit A"]

[echo "Commit B" >> file.txt]  
[git commit -am "commit B"]

[echo "Commit C" >> file.txt]  
[git commit -am "commit C"]

Check history:

[git log --oneline]

---

## 🔹 1️⃣ git reset --soft HEAD~1

Command:

[git reset --soft HEAD~1]

### 🔍 What Happened?

- Last commit (C) removed from commit history
- Changes from commit C remain in **staging area**
- File modifications are ready to re-commit

### ✅ Use Case

When you want to:
- Modify commit message
- Combine commits
- Adjust last commit without losing changes

---

## 🔹 2️⃣ git reset --mixed HEAD~1 (Default)

Command:

[git reset --mixed HEAD~1]

### 🔍 What Happened?

- Last commit removed
- Changes moved to **working directory**
- Changes are NOT staged

### ✅ Use Case

When you want to:
- Undo commit but re-edit files
- Selectively stage changes again

---

## 🔹 3️⃣ git reset --hard HEAD~1

Command:

[git reset --hard HEAD~1]

### 🔍 What Happened?

- Last commit removed
- Changes permanently deleted
- Working directory reset to previous commit state

⚠️ This is destructive.

---

## 📌 Reset Comparison

| Option | Removes Commit | Keeps Changes Staged | Keeps Changes in Working Dir | Safe? |
|--------|----------------|----------------------|-----------------------------|-------|
| --soft | ✅ Yes | ✅ Yes | ❌ No | ⚠️ Careful |
| --mixed | ✅ Yes | ❌ No | ✅ Yes | ⚠️ Careful |
| --hard | ✅ Yes | ❌ No | ❌ No | ❌ Dangerous |

---

## ❓ Answers

### What is the difference?

- --soft → undo commit, keep staged changes
- --mixed → undo commit, keep changes but unstaged
- --hard → undo commit and delete changes

### Which is destructive?

--hard is destructive because it permanently deletes uncommitted changes.

### When would you use each?

- --soft → fix last commit
- --mixed → redo staging process
- --hard → discard unwanted work completely

### Should you use reset on pushed commits?

❌ No.  
Reset rewrites history. If already pushed, it can break collaboration.

---

# ✅ Task 2: Git Revert — Hands-On

## 🔹 Step 1: Create 3 Commits (X, Y, Z)

[echo "Commit X" > file.txt]  
[git commit -am "commit X"]

[echo "Commit Y" >> file.txt]  
[git commit -am "commit Y"]

[echo "Commit Z" >> file.txt]  
[git commit -am "commit Z"]

---

## 🔹 Revert Middle Commit (Y)

Find commit hash:

[git log --oneline]

Revert:

[git revert <commit-hash-of-Y>]

---

### 🔍 What Happened?

- Git created a **new commit**
- That commit reverses changes made by Y
- Original commit Y still exists in history

Check:

[git log --oneline]

You will see:

commit Z  
Revert "commit Y"  
commit Y  
commit X  

---

## ❓ Answers

### How is revert different from reset?

- reset removes commit from history
- revert adds a new commit that reverses changes

### Why is revert safer?

Because it does NOT rewrite history.  
It keeps commit history intact.

### When to use revert vs reset?

Use revert:
- On shared branches
- After pushing commits

Use reset:
- On local commits
- Before pushing

---

# ✅ Task 3: Reset vs Revert Summary

| Feature | git reset | git revert |
|----------|------------|-------------|
| What it does | Moves HEAD backward | Creates reverse commit |
| Removes commit from history? | ✅ Yes | ❌ No |
| Safe for pushed branches? | ❌ No | ✅ Yes |
| Rewrites history? | ✅ Yes | ❌ No |
| Best used for | Local undo | Safe shared undo |

---

# ✅ Task 4: Branching Strategies

---

## 1️⃣ GitFlow

### 🔹 How it Works

Main branches:
- main (production)
- develop (integration)

Supporting branches:
- feature/*
- release/*
- hotfix/*

### 🔹 Flow Diagram

main  
 └── develop  
       ├── feature/login  
       ├── feature/payment  
       └── release/v1.0  
            └── hotfix/bug-1  

### 🔹 Used In

- Enterprise teams
- Structured release cycles

### 🔹 Pros

✔ Clear structure  
✔ Controlled releases  
✔ Parallel development  

### 🔹 Cons

✖ Complex  
✖ Heavy process  

---

## 2️⃣ GitHub Flow

### 🔹 How it Works

- Single main branch
- Create feature branch
- Open PR
- Merge after review

### 🔹 Flow

main  
 └── feature-1 → PR → merge  
 └── feature-2 → PR → merge  

### 🔹 Used In

- Startups
- SaaS products
- Continuous deployment

### 🔹 Pros

✔ Simple  
✔ Fast  
✔ Easy to manage  

### 🔹 Cons

✖ Less structured for scheduled releases  

---

## 3️⃣ Trunk-Based Development

### 🔹 How it Works

- Everyone commits to main
- Very short-lived branches
- Heavy CI/CD automation

### 🔹 Flow

main ← small commits ← developers  

### 🔹 Used In

- High-performing DevOps teams
- Companies with strong CI/CD

### 🔹 Pros

✔ Very fast delivery  
✔ Minimal merge conflicts  

### 🔹 Cons

✖ Requires strong automation  
✖ Risky without good testing  

---

## ❓ Answers

### Which strategy for a startup shipping fast?

✅ GitHub Flow

Because:
- Simple
- Quick PR process
- Fast deployments

---

### Which strategy for large team with scheduled releases?

✅ GitFlow

Because:
- Clear release planning
- Separate hotfix and release branches
- Controlled production deployments

---

### Which one do most open-source projects use?

Most open-source projects use GitHub Flow  
Example: Kubernetes, React, Terraform

---

# ✅ Task 5: Git Commands Reference (Days 22–25)

---

## 🔹 Setup & Config

[git config --global user.name "Your Name"]  
[git config --global user.email "your@email.com"]  
[git init]

---

## 🔹 Basic Workflow

[git status]  
[git add .]  
[git commit -m "message"]  
[git log --oneline]  
[git diff]

---

## 🔹 Branching

[git branch]  
[git branch feature-1]  
[git checkout feature-1]  
[git switch -c feature-2]

---

## 🔹 Remote

[git remote add origin <url>]  
[git push origin main]  
[git pull origin main]  
[git fetch]  
[git clone <repo-url>]

---

## 🔹 Merging & Rebasing

[git merge feature-branch]  
[git rebase main]

---

## 🔹 Stash & Cherry Pick

[git stash]  
[git stash pop]  
[git cherry-pick <commit-hash>]

---

## 🔹 Reset & Revert

[git reset --soft HEAD~1]  
[git reset --mixed HEAD~1]  
[git reset --hard HEAD~1]  
[git revert <commit-hash>]

---

# 🎯 Final Learning

Today I understood:

- Never fear mistakes in Git
- Use reset for local fixes
- Use revert for shared safety
- Choose branching strategy based on team size & release style

This completes Day 25 of my DevOps journey 🚀
