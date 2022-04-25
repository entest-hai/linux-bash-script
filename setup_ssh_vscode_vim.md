## Setup SSH with password 
**07 APR 2022 Hai Tran**
Edit
```
nano /etc/ssh/sshd_config
```
```
PermitRootLogin yes
```
Setup password 
```
sudo passwd ubuntu
```
```
sudo passwd root
```

## SSH into EC2 without password 
Generate private and public key 
```
ssh-keygen -t rsa -m PEM
```
Show the public key generated from the local machine 
```
cat ~/.ssh/id_rsa.pub 
```
Append the public key to EC2 to authorized_keys 
```
echo 'ssh-rsa AAAAB...' >> /home/ubuntu/.ssh/authorized_keys 
```
Add the key to ssh client at local 
```
ssh-add ~/.ssh/id_rsa
```
Test 
```
ssh ubuntu@13.214.81.16
```

## Setup vscode ssh into EC2 
