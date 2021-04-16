# NetworkManager DHCP-Server - Antwort 

```
/etc/NetworkManager/NetworkManager.conf 
level=TRACE
domains=ALL

# Restart des NetworkManager
systemctl restart NetworkManager 

journalctl -u NetworkManager | grep received | less 

# Apr 16 12:46:10 centos8-01 NetworkManager[28829]: <debug> [1618569970.5898] dhcp4 (enp0s8): received ACK of 192.168.56.101 from 0.0.0.0


```
