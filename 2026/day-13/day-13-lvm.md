# 💾 Linux Volume Management (LVM) – Hands-On Practice (Day 13)
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


Screenshot: <img width="518" height="171" alt="task2" src="https://github.com/user-attachments/assets/c01c32bd-b037-418c-b98a-6fcfba90a231" />


📦 Create Volume Group
vgcreate devops-vg /dev/sdb
vgs


Screenshot: <img width="545" height="130" alt="tast3" src="https://github.com/user-attachments/assets/c414a334-2dc8-4d91-81c1-97da32d39038" />


📑 Create Logical Volume
lvcreate -L 500M -n app-data devops-vg
lvs

Screenshot: <img width="997" height="142" alt="task4" src="https://github.com/user-attachments/assets/3e02de80-6c83-4216-ac8d-d6dd498013f2" />

🗂️ Format and Mount
mkfs.ext4 /dev/devops-vg/app-data
mkdir -p /mnt/app-data
mount /dev/devops-vg/app-data /mnt/app-data
df -h /mnt/app-data


Screenshot: <img width="757" height="386" alt="task5" src="https://github.com/user-attachments/assets/02940646-e7ef-4c49-907d-7f110956c461" />


📈 Extend the Volume
lvextend -L +200M /dev/devops-vg/app-data
resize2fs /dev/devops-vg/app-data
df -h /mnt/app-data


Screenshot: <img width="1107" height="305" alt="tast6" src="https://github.com/user-attachments/assets/ca8d87da-d7be-471c-b693-c7937e772408" />

📑 Documentation
Commands Used
- lsblk, pvs, vgs, lvs, df -h
- pvcreate, vgcreate, lvcreate
- mkfs.ext4, mount, lvextend, resize2fs

Screenshots:
(Attached all task-specific screenshots under each section above)

What I Learned
- How to create and manage Physical Volumes (PV), Volume Groups (VG), and Logical Volumes (LV).
- How to format and mount logical volumes for flexible storage usage.
- How to extend volumes live and resize filesystems without downtime.


---

✅ How to use this:
1. Copy everything inside the code block above.  
2. Paste it into your editor (VS Code, Notepad++, or GitHub).  
3. Save it as `day-13-lvm.md`.  
4. Replace the `your-screenshot-x` placeholders with your actual screenshot links.  





