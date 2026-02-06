# 💾 Linux Volume Management (LVM) – Hands-On Practice (Day 13)

---

### 📂 Storage Check
```bash
lsblk
pvs
vgs
lvs
df -h
<img width="603" height="286" alt="task-1" src="https://github.com/user-attachments/assets/136102c2-c4e5-4983-81f2-6bb069374d3d" />

🔨 Create Physical Volume
pvcreate /dev/sdb
pvs


<img width="518" height="171" alt="task2" src="https://github.com/user-attachments/assets/c01c32bd-b037-418c-b98a-6fcfba90a231" />

📦 Create Volume Group
vgcreate devops-vg /dev/sdb
vgs


<img width="545" height="130" alt="task3" src="https://github.com/user-attachments/assets/c414a334-2dc8-4d91-81c1-97da32d39038" />
