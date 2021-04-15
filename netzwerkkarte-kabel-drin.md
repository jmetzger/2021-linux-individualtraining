# Netzwerkkarte - Kabel drin ? 

```
# Variant 1 (Centos/Redhat  && Ubuntu/Debian) 
ip link show enp0s8 

# If cable it not plugin-in 
NO-CARRIER 

# Variant 2: Works on all systems  
cat /sys/class/net/enp0s8/operstate

# Variant 3: nmcli (Centos/Redhat) 
nmcli conn show  # Alle Connections 
nmcli dev show  # Alle Netzwerk-Devices 
```
