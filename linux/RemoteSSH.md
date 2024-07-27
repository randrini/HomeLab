### *Remote SSH from Linux to Windows*

Activate OpenSSH from Windows Features

Start sshd and ssh-agent service

Set services start to automatic


From Linux

=> Generate cert pair with ssh-keygen

Upload id_rsa.pub to Windows via sftp

Append id_rsa.pub content to $env:USERPROFILE\.ssh\authorized_keys file

Append id_rsa.pub content to %programdata%\***\admin_authorized_keys file

Limit access to those 2 files to Administartors group only

Test
