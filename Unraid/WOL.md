# ⚙️ **Configure Unraid Sleep**

Follow these steps to install and configure the Dynamix S3 Sleep plugin:

### 1️⃣ **Install the Plugin**
- Install the **Dynamix S3 Sleep** plugin.

### 2️⃣ **Set Wake On LAN**
- Set **Wake On LAN** to **g**.

### 3️⃣ **Configure Network Settings**
- Add the following line to your `/config/go` file:
  ```bash
  ethtool -s eth0 wol g
  ```
