# 🌟 Alpine Linux CT Setup Guide 🌟

To configure Alpine Linux with Tailscale and IP forwarding, follow these steps:

```bash
# Enable Tailscale Service (if needed)
rc-update add tailscale && rc-service tailscale restart

# Enable IPv4 forwarding
echo 'net.ipv4.ip_forward = 1' | tee -a /etc/sysctl.d/99-tailscale.conf

# Enable IPv6 forwarding
echo 'net.ipv6.conf.all.forwarding = 1' | tee -a /etc/sysctl.d/99-tailscale.conf

# Apply the new configuration
sysctl -p /etc/sysctl.d/99-tailscale.conf

# Add sysctl to services
rc-update add sysctl

# Restart sysctl service
rc-service sysctl restart

# Reboot system to apply changes
reboot
