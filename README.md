 # SETTING UP A SCALABLE FILE STORAGE SYSTEM USING AMAZON ELASTIC FILE SYSTEM
  ## AIM
       To  setting up a scalable file storage system using Amazon Elastic File System (EFS) for two EC2 instances in different availability zones. 
## PROBLEM STATEMENT
    This experiment demonstrates how to configure Amazon EFS to provide a shared storage solution for two Linux EC2 instances across different availability zones, enabling easy data sharing. The aim is to ensure both instances can mount 
     and access the EFS file system and validate data consistency across instances.

## ALGORITHM
 ### Steps 1: Create two EC2 instances in different availability zones.
 ### Steps 2: Set up a security group that allows necessary communication between the instances and EFS.
 ### Steps 3: Create an EFS file system and mount it to both EC2 instances.
 ### Steps 4: Ensure that the EC2 instances can access the file system and share data between them.

## COMMANDS
### EC2 Instance 1
```
sudo su
yum install httpd -y
yum install -y amazon-efs-utils
mount -t efs -o tls fs-064645ac116a12816:/ /var/www/html
cd /var/www/html
vi file  # Create a file and add some text
```
### EC2 Instance 2
```
sudo su
yum install httpd -y
yum install -y amazon-efs-utils
mount -t efs -o tls fs-064645ac116a12816:/ /var/www/html
cd /var/www/html
ls
cat file  # Verify shared access by reading content created in Instance 1
```
### REGISTER NUMBER: 212222040087
### NAME : Lokesh K
## OUTPUT
### Both EC2 instances showing EFS mounting.
![image](https://github.com/user-attachments/assets/912f1d2a-1494-4863-ae26-9e36cd637628)
![image](https://github.com/user-attachments/assets/cbc5fc79-baa6-4d54-853e-8a35cbcff2c5)
![image](https://github.com/user-attachments/assets/51ef3224-2139-4508-a935-b11820263b7a)
![image](https://github.com/user-attachments/assets/d0e788dc-6e6e-4785-bd9a-0cafc26e88d2)
![image](https://github.com/user-attachments/assets/4d49e331-b666-40ff-9166-a51972dc589e)

## RESULT
Thus, The setting up a scalable file storage system using Amazon Elastic File System (EFS) for two EC2 instances in different availability zones, enabling shared access to data is executed successfully.
