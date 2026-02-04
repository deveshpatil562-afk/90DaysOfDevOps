# 🗓️ Day 11 – File Ownership Challenge (chown & chgrp)

## 🚀 Overview
Day 11 was all about **file ownership and group management in Linux**.  
I practiced creating files and directories, assigning users and groups, and verifying permissions using different `ls` options. This challenge helped me understand how ownership works in real-world, multi-user environments.

---

## 📂 Files & Directories Created

### 📁 Directories
- `ubuntu/` *(pre-existing, shown in outputs)*
- `app-logs/`
- `heist-project/`
  - `vault/`
  - `plans/`
- `bank-heist/`

### 📄 Files
- `devops-file.txt`
- `team-notes.txt`
- `project-config.yaml`
- `heist-project/vault/gold.txt`
- `heist-project/plans/strategy.conf`
- `bank-heist/access-codes.txt`
- `bank-heist/blueprints.pdf`
- `bank-heist/escape-plan.txt`

---

## 🗂️ Ownership Changes

### 🔁 File Ownership Updates

| File | Original Owner | Updated Owner |
|----|----|----|
| `devops-file.txt` | `root:root` | `tokyo:root` → `berlin:root` |
| `team-notes.txt` | `root:root` | `root:heist-team` |
| `project-config.yaml` | `root:root` | `professor:heist-team` |

---

### 📁 Directory Ownership Updates

#### `app-logs/`
- `root:root` → `berlin:heist-team`

#### `heist-project/` *(Recursive Ownership Change)*
- `plans/strategy.conf` → `professor:planners`
- `vault/gold.txt` → `professor:planners`
- `plans/` directory → `professor:planners`
- `vault/` directory → `professor:planners`

---

### 🏦 `bank-heist/` (Individual File Ownership)

| File | New Ownership |
|----|----|
| `access-codes.txt` | `tokyo:vault-team` |
| `blueprints.pdf` | `berlin:tech-team` |
| `escape-plan.txt` | `nairobi:vault-team` |

---

## 🧠 Commands Used & Purpose

| Command | Description |
|------|------------|
| `ls -l` | List files with permissions, owner, group, size, and timestamp |
| `ls -lh` | Same as `ls -l` but with human-readable file sizes |
| `ls -ltra` | List all files sorted by time, including hidden files |
| `ls -LR` | Recursively list directories and their contents |
| `sudo touch <file>` | Create a file with root privileges |
| `sudo mkdir <dir>` | Create a directory with root privileges |
| `sudo mkdir -p <path>` | Create nested directories |
| `sudo chown <user> <file>` | Change file owner |
| `sudo chown <user>:<group> <file>` | Change file owner and group |
| `sudo chown -R <user>:<group> <dir>` | Recursively change ownership |
| `sudo chgrp <group> <file>` | Change group ownership |
| `sudo groupadd <group>` | Create a new group |
| `cd <dir>` | Change directory |
| `cd ..` | Move up one directory |
| `cd .` | Stay in the current directory |

---

## ✅ What I Learned

### 📁 Creating Files & Directories
I gained confidence using `touch`, `mkdir`, and `mkdir -p` to build structured project environments from scratch.

### 👥 Managing Ownership & Groups
I practiced using `chown` and `chgrp` to control file and directory ownership. Applying **recursive ownership changes** helped me understand how permissions scale in real systems.

### 🔍 Verification & Navigation
I explored multiple `ls` options (`-l`, `-lh`, `-ltra`, `-LR`) to verify ownership and permissions and navigated directories efficiently using `cd`.

---

## 🎯 Key Takeaway
File ownership is a **critical part of Linux security and collaboration**.  
This challenge gave me hands-on experience managing users, groups, and permissions in a structured, real-world-style scenario.

---

💡 *Day 11 complete — moving one step closer to Linux mastery!*
