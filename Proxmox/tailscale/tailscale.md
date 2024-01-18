Alpine Linux CT

Add IP forwarding
  echo 'net.ipv4.ip_forward = 1' | tee -a /etc/sysctl.d/99-tailscale.conf
  echo 'net.ipv6.conf.all.forwarding = 1' | tee -a /etc/sysctl.d/99-tailscale.conf
  sysctl -p /etc/sysctl.d/99-tailscale.conf

Add sysctl as service !!
  rc-update add sysctl
  rc-service systcl restart

Reboot
reboot

Test
