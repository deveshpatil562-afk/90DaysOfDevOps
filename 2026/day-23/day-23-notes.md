# 📘 Day 23 – Git Branching & Working with GitHub

## 🎯 Task Overview

Now that I understand how to create repositories, stage files, and commit changes — it's time to learn one of the most powerful features in Git: **Branching**.

Branches allow developers to work on features, bug fixes, or experiments in isolation without affecting the main codebase. This ensures stability and clean collaboration.

---

# ✅ Expected Output

- Created `day-23-notes.md`
- Updated `git-commands.md` inside `devops-git-practice` repo
- Successfully pushed local repository to GitHub

---

# 🚀 Challenge Tasks

---

## 🧠 Task 1: Understanding Branches

### 1️⃣ What is a branch in Git?

A branch in Git is a movable pointer to a specific commit. It allows you to create separate lines of development inside the same repository.

---

### 2️⃣ Why do we use branches instead of committing everything to main?

- To avoid breaking production code  
- To develop features independently  
- To test changes safely  
- To collaborate with multiple developers  
- To maintain a clean version history  

---

### 3️⃣ What is HEAD in Git?

`HEAD` is a pointer that refers to the currently checked-out branch or commit.  
It tells Git where you are currently working.

---

### 4️⃣ What happens when you switch branches?

- Git updates your working directory  
- Files change to match the selected branch  
- Commits unique to other branches disappear from view  
- Your codebase reflects that branch’s state  

---

# 🔧 Task 2: Branching Commands — Hands-On

Below are the commands performed inside `devops-git-practice`.

---

### 📌 List all branches

[git branch]

---

### 📌 Create a new branch called feature-1

[git branch feature-1]

---

### 📌 Switch to feature-1

[git checkout feature-1]

---

### 📌 Create and switch in a single command (feature-2)

[git checkout -b feature-2]

---

### 📌 Using modern switch command

[git switch main]  
[git switch feature-1]

👉 Difference:
- `git checkout` is older and used for switching branches AND restoring files.
- `git switch` is newer and specifically designed only for branch switching (safer & clearer).

---

### 📌 Make a commit on feature-1

[echo "Feature 1 work" >> feature.txt]  
[git add feature.txt]  
[git commit -m "Added feature-1 changes"]

---

### 📌 Switch back to main and verify

[git switch main]

The commit made on `feature-1` does NOT appear on `main`.

---

### 📌 Delete a branch

[git branch -d feature-2]

---

### 📌 Add all commands to git-commands.md

[vi git-commands.md]

---

# 🌍 Task 3: Push to GitHub

---

### 📌 Create GitHub repository (without README)

Repository created manually on GitHub.

---

### 📌 Connect local repo to remote

[git remote add origin https://github.com/<your-username>/devops-git-practice.git]

---

### 📌 Push main branch

[git push -u origin main]

---

### 📌 Push feature-1 branch

[git push -u origin feature-1]

---

### 📌 Verify branches on GitHub

Checked on GitHub UI — both `main` and `feature-1` are visible.

---

### ❓ Difference between origin and upstream

- `origin` → Default name for YOUR remote repository.
- `upstream` → Refers to the original repository you forked from.

---

# 🔄 Task 4: Pull from GitHub

---

### 📌 Make change directly on GitHub

Edited file using GitHub web editor.

---

### 📌 Pull changes locally

[git pull origin main]

---

### ❓ Difference between git fetch and git pull

- `git fetch` → Downloads changes but does NOT merge.
- `git pull` → Fetch + Merge in one command.

---

# 🔁 Task 5: Clone vs Fork

---

### 📌 Clone a public repository

[git clone https://github.com/user/repository.git]

---

### 📌 Fork repository on GitHub

Forked using GitHub UI → then cloned fork.

---

### ❓ Difference between Clone and Fork

| Clone | Fork |
|-------|------|
| Git command | GitHub feature |
| Creates local copy | Creates server-side copy under your account |
| Used for working locally | Used for contributing to other projects |

---

### ❓ When to clone vs fork?

- Clone → When you have direct access to repository.
- Fork → When contributing to open-source projects without direct write access.

---

### ❓ After forking, how to keep fork in sync?

[git remote add upstream https://github.com/original-owner/repo.git]  
[git fetch upstream]  
[git merge upstream/main]

---

# 📝 Key Takeaways

✔ Branches allow safe and isolated development  
✔ `git switch` is modern and safer than `git checkout`  
✔ `origin` and `upstream` serve different collaboration purposes  
✔ `git fetch` gives more control than `git pull`  
✔ Forking is a GitHub workflow concept  

---

# 📌 Final Status

✅ Branches created and tested  
✅ Commands documented  
✅ Repository pushed to GitHub  
✅ Clone & Fork practiced  

---

🔥 Day 23 Completed — Mastering Git Branching & GitHub Workflow 🔥
