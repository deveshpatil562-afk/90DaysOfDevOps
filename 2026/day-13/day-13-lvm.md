# 📌 Day 13 – Linux Volume Management (LVM)

## 🎯 Task
Learn LVM to manage storage flexibly – create, extend, and mount volumes.

---

## 🚀 Challenge Tasks

### Task 1: Check Current Storage
Commands:
```bash
lsblk
pvs
vgs
lvs
df -h

<img width="603" height="286" alt="task-1" src="https://github.com/user-attachments/assets/26315be5-1a5c-423b-9116-78434f07eac0" />


### Task 2: Create Physical volume 
Commands:
pvcreate /dev/sdb   # or your loop device
pvs

<img width="518" height="171" alt="task2" src="https://github.com/user-attachments/assets/20f7ded0-c296-495d-a6b2-2149c8bb4af5" />


### Task 3: Create Volume Group
Commands:
vgcreate devops-vg /dev/sdb
vgs

<img width="545" height="130" alt="tast3" src="https://github.com/user-attachments/assets/43dca167-652b-4ee2-8498-176b30515055" />


### Task 4: Create logical volume 
Commands:
lvcreate -L 500M -n app-data devops-vg
lvs

<img width="997" height="142" alt="task4" src="https://github.com/user-attachments/assets/3ee1d437-754e-49cc-8a92-8deb3eef45ca" />


### Task 5: Format and Mount
Commands:
mkfs.ext4 /dev/devops-vg/app-data
mkdir -p /mnt/app-data
mount /dev/devops-vg/app-data /mnt/app-data
df -h /mnt/app-data

<img width="757" height="386" alt="task5" src="https://github.com/user-attachments/assets/1711bbc4-2b89-4e77-a520-64935ea43e2e" />


### Task 6: Extend volume
Commands:
lvextend -L +200M /dev/devops-vg/app-data
resize2fs /dev/devops-vg/app-data
df -h /mnt/app-data

<img width="1107" height="305" alt="tast6" src="https://github.com/user-attachments/assets/65673279-4f53-4d5b-9eb6-b1def44e4369" />


### What I Learned
- How to create and manage Physical Volumes (PV), Volume Groups (VG), and Logical Volumes (LV).
- How to format and mount logical volumes for flexible storage usage.
- How to extend volumes live and resize filesystems without downtime

