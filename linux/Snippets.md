# 🔍 **Search for a String in All Directories**

### 1️⃣ **Enable IPv4 Forwarding**
- To check if IPv4 forwarding is enabled, run the following commands:

```bash
# Search for IPv4 forwarding settings
nice -19 grep -airlE 'net.ipv4.ip_forward|/proc/sys/net/ipv4/ip_forward' /
grep -rn net.ipv4.ip_forward /etc/*
```

---

# 📁 **Transfer Files Using SFTP**

### 2️⃣ **Copy Files to Another Linux Machine**
- To connect and copy files via SFTP:

```bash
sftp root@192.168.1.100
get filename
get -r recursiveFolder/
```

### 3️⃣ **Copy Over SSH**
- Navigate to your local directory and connect using SFTP:

```bash
cd Documents
sftp sammy@your_server_ip_or_remote_hostname
cd NASA/secret_files/
get UFO_blueprint.odt
get -r secret_files/
```
