Alpine Linux CT

Add IP forwarding
echo net.ipv4.ip_forward=1 | tee -a /etc/sysctl.conf && sysctl -p
