# 🔒 **Remote SSH from Linux to Windows**

Follow these steps to set up remote SSH access from Linux to Windows:

#### 1️⃣ **From Windows**
- Activate **OpenSSH** from Windows Features.
- Start the **sshd** and **ssh-agent** services.
- Set these services to start automatically.

---

#### 2️⃣ **From Linux**
- Generate a key pair with `ssh-keygen`.
- Change directory to the key pair location.
- Upload `id_rsa.pub` to Windows via SFTP:
  ```bash
  put id_rsa.pub C:\ProgramData\ssh\
  ```
- ~~Append `id_rsa.pub` content to `$env:USERPROFILE\.ssh\authorized_keys` file~~
- Append `id_rsa.pub` content to `%programdata%\ssh\admin_authorized_keys` file .
- Limit access to these two files to the **Administrators** group only.
- Specify the config file with `-i /config/.ssh/id_privatekey` and set permissions:
  ```bash
  chmod 600 id_privatekey
  ```
- Delete `id_rsa.pub` to clean up.
