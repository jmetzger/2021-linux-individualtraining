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
# Show only active connection (activated with nmtui) 
nmcli conn show --active 
nmcli conn show enp0s8 
# Kabel gezogen 
nmcli dev show enp0s8 
# -> must have: ...CARRIER: aus/an 
nmcli dev show enp0s8 | grep -i carrier  # -i -> case insensitive -> egal ob gross oder klein geschrieben
# 
nmcli -f WIRED-PROPERTIES dev show enp0s8 
#
```

## Netzwerkkarte aktivieren / deaktivieren nmcli 

```
nmcli conn show
# Das wäre das gleich wie aktivieren/deaktivieren in nmtui 
# Achtung . muss der Name der Connection sein und nicht Interface
# Auf centos8 testsystem war das identisch 
nmcli conn up enp0s8 
nmcli conn down enp0s8
```
