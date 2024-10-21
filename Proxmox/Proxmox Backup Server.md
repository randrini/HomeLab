# 🛠️ **Create Privileged LXC Container on Proxmox VE**

Follow these steps to create a privileged LXC container on PVE:

### 1️⃣ **Create the LXC Container**
- Choose **Debian 12** as the template.
- Set the **root password** for the container.

### 2️⃣ **Access the LXC Shell**
- Run the following commands:

```bash
# Execute the Tteck post PBS install script and reboot
bash <(curl -s https://path_to_script) && reboot

# Install NFS common package
apt update && apt install nfs-common -y

# Create the mount directory
mkdir -p /mnt/unraid/proxmox

# Configure fstab for NFS mount
echo '192.168.1.116:/mnt/user/backups/proxmox /mnt/unraid/proxmox nfs defaults 0 0' | tee -a /etc/fstab

# Reboot the container
reboot
```

### 3️⃣ **Add Datastore in Proxmox Backup Server**
- Add a datastore with the absolute path `/mnt/unraid/proxmox` and name it **Unraid**.
- Create a PBS user for PVE backup with the username **pbs**.

### 4️⃣ **Configure Storage on Proxmox VE**
- Go to **Datacenter** in the Proxmox web interface.
- Add storage:
  - **Type:** Proxmox Backup Server
  - **User:** pbs
  - **Datastore:** Unraid
  - **Namespace:** backups

### 5️⃣ **Set Up Backup Schedule**
- Go to **Datacenter**.
- Add a backup job and select a schedule.
