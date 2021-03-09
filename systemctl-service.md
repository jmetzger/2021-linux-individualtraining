# Systemctl / Service 

## systemctl Beispiele 
```
# Status eines Dienstes überprüfen 
service sshd status 
systemctl status sshd 

# Wie heisst der Dienst / welche Dienste gibt es ? 
systemctl list-units -t service 
# für apache
systemctl list-units -t service | grep ^apache
# die Abkürzung 
systemctl -t service | grep ^apache


# Dienst aktivieren
systemctl enable apache2 
# Ist Dienst aktiviert 
systemctl is-enabled apache2
enabled
echo $?
0 # Wenn der Dienst aktiviert ist 

# Dienst deaktivieren (nach Booten nicht starten)
systemctl disable apache2
systemctl is-enabled 
disabled
echo $?
1 # 1 wenn nicht aktiviert

# Rebooten des Servers
# verweist auf systemctl 
reboot
systemctl reboot
shutdown -r now  

# Halt (ohne Strom ausschalten) 
halt
systemctl halt 
shutdown -h now 

# Poweroff 
poweroff
systemctl poweroff 
```

## Welche Dienste sind aktiviert/deaktiviert 
```
systemctl list-unit-files -t service
```

## systemctl Cheatsheet 

  * https://access.redhat.com/sites/default/files/attachments/12052018_systemd_6.pdf
