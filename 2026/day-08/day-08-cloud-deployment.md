**Today's goal is to deploy a real web server on the cloud and learn practical server management.**

Step 1:
Create an AWS EC2 Instance:

<img width="1906" height="767" alt="image" src="https://github.com/user-attachments/assets/f9aaf50f-ab61-45c1-be25-fd397cc7299f" />


Step 2:
Login using SSH Client to server:

<img width="1446" height="437" alt="image" src="https://github.com/user-attachments/assets/07c211ab-e59d-4b13-888e-42f7598182f8" />


Step 3:
Install nginx and docker to the server.
Commands:
#sudo apt install nginx
#sudo apt install docker.io

<img width="923" height="403" alt="image" src="https://github.com/user-attachments/assets/c71d3536-9a5a-4ad2-8840-96ff3858d77d" />


Step 4:
Add Inbound rule of port 80 to the server in "Security" tab of EC2 Server.

<img width="1916" height="808" alt="image" src="https://github.com/user-attachments/assets/db2dbecd-52fc-4ea1-982c-1efb17e9c283" />


Step 5:
we will save the logs of nginx to our local computer using below command:
#scp -i "C:\Users\91930\Downloads\devesh-aws-key.pem" ubuntu@ec2-18-222-8-254.us-east-2.compute.amazonaws.com:/home/ubuntu/nginx-logs.txt .

<img width="1852" height="386" alt="image" src="https://github.com/user-attachments/assets/887cd4c8-36bf-46c8-bf3c-ef05eff7f775" />


Step 6:
Copy public ip and run with port 80 to check nginx connection.

<img width="1748" height="380" alt="image" src="https://github.com/user-attachments/assets/2b876f10-ccfa-429b-a0a4-1ca9a5b69ac0" />




