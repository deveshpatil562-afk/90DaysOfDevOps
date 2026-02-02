**Hand Written notes of User and Group Management:-**


<img width="1280" height="1265" alt="image" src="https://github.com/user-attachments/assets/239cfd6c-8e0e-4c3d-b1d4-d99fcb8299b9" />


<img width="952" height="1280" alt="image" src="https://github.com/user-attachments/assets/7627b07c-f7b1-4ce8-8ec7-f7a53a8d8a04" />


<img width="960" height="1280" alt="image" src="https://github.com/user-attachments/assets/8b578ef7-5765-4886-a28b-7136a29cf764" />


<img width="960" height="1280" alt="image" src="https://github.com/user-attachments/assets/b7f32560-f3fe-493d-99b1-cba8ef1da362" />


<img width="960" height="1280" alt="image" src="https://github.com/user-attachments/assets/e56dc09e-fed6-469e-906c-37a985638748" />


<img width="1280" height="660" alt="image" src="https://github.com/user-attachments/assets/15b68f36-89e9-4b54-bfc7-ac1e26c20aca" />




**Practice Task of User And Group Management:**

# Day 09 Challenge

## Note: I have created group "tester" instead of "admin"

## Users & Groups Created
- Users: tokyo, berlin, professor, nairobi
- Groups: developers, admins, project-team

## Group Assignments
ubuntu@ip-172-31-9-231:~$ id tokyo
uid=1002(tokyo) gid=1002(tokyo) groups=1002(tokyo),1004(developers),1007(project-team)
ubuntu@ip-172-31-9-231:~$ id berlin
uid=1001(berlin) gid=1001(berlin) groups=1001(berlin),1004(developers),1005(testers)
ubuntu@ip-172-31-9-231:~$ id professor
uid=1003(professor) gid=1003(professor) groups=1003(professor),1005(testers)
ubuntu@ip-172-31-9-231:~$ id nairobi
uid=1004(nairobi) gid=1006(nairobi) groups=1006(nairobi),1007(project-team)


## Directories Created
ubuntu@ip-172-31-9-231:~$ ls -ld /opt/team-workspace
drwxrwxr-x 2 root project-team 4096 Feb  2 07:50 /opt/team-workspace
ubuntu@ip-172-31-9-231:~$ ls -ld /opt/dev-project
drwxrwxr-x 2 root developers 4096 Feb  2 07:36 /opt/dev-project

## Commands Used
useradd Tokyo
groupadd developers
gpasswd -a Tokyo to developers
mkdir /opt/dev-project
chgrp developer /opt/dev-project
chmod 775 /opt/dev-project
sudo -u tokyo touch /opt/dev-project/tokyo.txt


## What I Learned
1)About user permissions and its importance
2)Same for group management
3)directories permission and its importance

## Outputs:

<img width="897" height="240" alt="Screenshot 2026-02-02 124607" src="https://github.com/user-attachments/assets/698c2d39-215c-4a29-9465-3983e630502e" />


<img width="777" height="141" alt="Screenshot 2026-02-02 130121" src="https://github.com/user-attachments/assets/9bc1d54f-975a-4b4f-abbc-aa545434f21d" />


<img width="1137" height="461" alt="Screenshot 2026-02-02 130230" src="https://github.com/user-attachments/assets/ea19976d-c89d-43b9-9a17-a998d556780c" />


<img width="1017" height="192" alt="Screenshot 2026-02-02 131052" src="https://github.com/user-attachments/assets/0c9aa886-b9cf-4934-8e8c-9da6e031687b" />


<img width="953" height="170" alt="Screenshot 2026-02-02 131602" src="https://github.com/user-attachments/assets/42fd87ee-239f-4a55-9358-8eb728c1c004" />


<img width="1042" height="328" alt="Screenshot 2026-02-02 132245" src="https://github.com/user-attachments/assets/be270b13-eb5f-4a50-93fc-a1106d1e2c71" />


<img width="982" height="292" alt="Screenshot 2026-02-02 132310" src="https://github.com/user-attachments/assets/b0d3fb18-1531-4c04-bdf9-13808fc3b2b2" />
