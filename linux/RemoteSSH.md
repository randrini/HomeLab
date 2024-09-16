### *Remote SSH from Linux to Windows*

#### 1. From Windows
- Activate OpenSSH from Windows Features
- Start sshd and ssh-agent service
- Set services start to automatic

---
#### 2. From Linux

- Generate cert pair with ssh-keygen
- cd to the cert pair location
- Upload id_rsa.pub to Windows via sftp with put id_rsa.pub to C:\ProgramData\ssh\
- <del>Append id_rsa.pub content to $env:USERPROFILE\.ssh\authorized_keys file</del>
- Append id_rsa.pub content to %programdata%\ssh\admin_authorized_keys file
- Limit access to those 2 files to Administartors group only
- Specify config file with -i /config/.ssh/id_privatekey and chmod 600 id_privatekey
- Delete id_rsa.pub
