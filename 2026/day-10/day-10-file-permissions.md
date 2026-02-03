## Hand Written Notes of File Permissions:

<img width="1600" height="1040" alt="image" src="https://github.com/user-attachments/assets/dd0806f5-0e12-4cf9-b469-fafa498d0c9d" />


<img width="1598" height="1600" alt="image" src="https://github.com/user-attachments/assets/abda7c35-f204-4a2f-b754-b6acadfe2637" />


## Practice:

# Day 10 Challenge

## Files Created

1)devops.txt
2)notes.txt
3)script.sh

## Permission Changes

- Make script.sh executable
→ chmod +x script.sh
- Test execution failure by removing execute permission
→ chmod 600 script.sh
- Set devops.txt to read‑only (remove write for all)
→ chmod a-w devops.txt
- Set notes.txt to 640 (owner: rw, group: r, others: none)
→ chmod 640 notes.txt
- Create directory project/ with permissions 755
→ chmod 755 project

## Commands Used

touch devops.txt
echo "Hi Everyone, Today we are practicing files permission on killer coda platform" > notes.txt
vim script.sh
ls -l
cat notes.txt
vim script.sh   (opened in read-only mode later)
cat /etc/passwd | head -n 5
cat /etc/passwd | tail -n 5
ls -ltra
./script.sh
mkdir project

## What I Learned

- Permissions Control Access
- The rwxrwxrwx format defines who can read, write, or execute a file.
- Owner, group, and others each have separate rights, and changing them directly impacts what actions are allowed.
- Execution Requires x Permission
- Even if a script has content, it cannot run unless the execute bit is set.
- Removing x leads to the “Permission denied” error, which is a common and important lesson in Linux administration.
- Error Messages Are Learning Tools
- Warnings like “readonly file” in Vim or “Permission denied” when running a script are not failures—they’re signals showing exactly what permission is missing.
- Understanding these messages helps you troubleshoot quickly and document best practices.

## Ouputs:

<img width="1005" height="232" alt="Screenshot 2026-02-03 124718" src="https://github.com/user-attachments/assets/63c35add-4da8-434b-8e54-d74c08baed85" />

<img width="761" height="357" alt="Screenshot 2026-02-03 125057" src="https://github.com/user-attachments/assets/fedb07ce-6adc-47bd-9672-0f71fa2f610d" />

<img width="578" height="565" alt="Screenshot 2026-02-03 125616" src="https://github.com/user-attachments/assets/bfb32b6a-eea2-44c3-ae7c-35aaaafa58c6" />

<img width="697" height="170" alt="Screenshot 2026-02-03 125744" src="https://github.com/user-attachments/assets/24b57c03-5a67-4362-81ed-432182e34b6d" />

<img width="381" height="105" alt="Screenshot 2026-02-03 125845" src="https://github.com/user-attachments/assets/43911473-1ed6-45b3-a0b4-fb644ea0e5fc" />
