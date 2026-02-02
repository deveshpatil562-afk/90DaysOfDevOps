# 🐧 Linux User & Group Management – Hands-On Practice (Day 09)

This repository documents my **hands-on Linux practice** focused on **User, Group, and Permission Management**.  
The task simulates a **real multi-user environment**, demonstrating how Linux controls access using users, groups, and directory permissions.

---

## 🚀 Skills Demonstrated
- Linux user management (`useradd`, `id`)
- Group creation and assignments
- Directory ownership and permissions
- Access validation using real users
- Practical Linux administration concepts

---

## 🧠 Learning Resources (Handwritten Notes)

These notes were created during my learning process to understand Linux access control deeply:

<p align="center">
  <img src="https://github.com/user-attachments/assets/239cfd6c-8e0e-4c3d-b1d4-d99fcb8299b9" width="45%" />
  <img src="https://github.com/user-attachments/assets/7627b07c-f7b1-4ce8-8ec7-f7a53a8d8a04" width="45%" />
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/8b578ef7-5765-4886-a28b-7136a29cf764" width="45%" />
  <img src="https://github.com/user-attachments/assets/b7f32560-f3fe-493d-99b1-cba8ef1da362" width="45%" />
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/e56dc09e-fed6-469e-906c-37a985638748" width="45%" />
  <img src="https://github.com/user-attachments/assets/15b68f36-89e9-4b54-bfc7-ac1e26c20aca" width="45%" />
</p>

---

## 🧪 Practice Task – Day 09 Challenge

> ⚠️ **Note:** I created a group named `testers` instead of `admins`.

### 👤 Users Created
- `tokyo`
- `berlin`
- `professor`
- `nairobi`

### 👥 Groups Created
- `developers`
- `testers`
- `project-team`

### Commands Output:

![1770020012602](https://github.com/user-attachments/assets/ca78ad70-5ff1-4329-b0f5-f5495b11b38e)



---

## 🔗 User & Group Assignments

```bash
id tokyo
uid=1002(tokyo) gid=1002(tokyo) groups=tokyo,developers,project-team

id berlin
uid=1001(berlin) gid=1001(berlin) groups=berlin,developers,testers

id professor
uid=1003(professor) gid=1003(professor) groups=professor,testers

id nairobi
uid=1004(nairobi) gid=1006(nairobi) groups=nairobi,project-team

## Directories Created:

ls -ld /opt/team-workspace
drwxrwxr-x 2 root project-team 4096 Feb 2 07:50 /opt/team-workspace

ls -ld /opt/dev-project
drwxrwxr-x 2 root developers 4096 Feb 2 07:36 /opt/dev-project


## Executed Commands:

# Create users and groups
useradd tokyo
groupadd developers

# Add user to group
gpasswd -a tokyo developers

# Create project directory
mkdir /opt/dev-project

# Assign group ownership
chgrp developers /opt/dev-project

# Set directory permissions
chmod 775 /opt/dev-project

# Validate access as a normal user
sudo -u tokyo touch /opt/dev-project/tokyo.txt




## 🎯 Key Learnings

Linux user permissions are critical for system security

Groups simplify access control in team environments

Correct directory permissions enable safe collaboration

Real-user testing validates permission configurations
