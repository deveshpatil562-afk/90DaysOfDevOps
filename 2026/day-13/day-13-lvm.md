# Day 13 – Linux Volume Management (LVM)

## 🎯 Objective
Learn how to use **Linux Logical Volume Management (LVM)** to manage storage flexibly by creating, mounting, and extending logical volumes.

---

## 🛠️ Challenge Tasks – Commands Used
```bash
# Switch to root user
sudo -i

# Task 1: Check current storage
lsblk
pvs
vgs
lvs
df -h

# Task 2: Create Physical Volume
pvcreate /dev/sdb
pvs

# Task 3: Create Volume Group
vgcreate devops-vg /dev/sdb
vgs

# Task 4: Create Logical Volume
lvcreate -L 500M -n app-data devops-vg
lvs

# Task 5: Format and mount the Logical Volume
mkfs.ext4 /dev/devops-vg/app-data
mkdir -p /mnt/app-data
mount /dev/devops-vg/app-data /mnt/app-data
df -h /mnt/app-data

# Task 6: Extend the Logical Volume
lvextend -L +200M /dev/devops-vg/app-data
resize2fs /dev/devops-vg/app-data
df -h /mnt/app-data

## Screenshots

<img width="603" height="286" alt="task-1" src="https://github.com/user-attachments/assets/21f639f9-9a76-44b1-8c04-00b6c5be817d" />
