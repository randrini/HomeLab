# 🚀 **Setup the VPS**

### 1️⃣ **Create a New Instance**
- Create a new instance:
  - Select **Free Tier Compute**.
  - Choose **Ubuntu**.

### 2️⃣ **Create New Networking**
- Set up a **Virtual Cloud Network (VCN)**:
  - Change the **VCN** and **VNIC** name.

### 3️⃣ **Set Up a Security List**
- Add a new ingress rule:
  - **Source:** `0.0.0.0/0`
  - **Protocol:** TCP
  - **Destination Port Range:** `22` (SSH)

- Add another ingress rule:
  - **Source:** `0.0.0.0/0`
  - **Protocol:** TCP
  - **Destination Port Range:** `3001` (Uptime Kuma)

- Click **Add Ingress Rules**.

---

# 🐳 **Install Docker**

### 4️⃣ **Install UptimeKuma via Docker Compose**

### 5️⃣ **Use CF Zero Trust Tunnel**
- Host `xxxx.owndomain.fr` on port `3001`.

### 6️⃣ **Install Tailscale with Split DNS**
