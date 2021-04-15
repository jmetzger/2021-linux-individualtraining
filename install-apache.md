# Install apache 

## Walkthrough 

```
## Schritt 1:
# suche // apache heisst auf centos httpd
yum search httpd
# oder
dns search httpd

## Schritt 2: 
yum install httpd 

## Wie heisst der Dienst und Starten und Enablen (für nächsten Reboot)  
yum list-unit-files --type=service | grep httpd
systemctl enable httpd 
systemctl start httpd 

## Schritt 3: 
# Konfiguration anpassen
# /etc/httpd/conf/httpd.conf # Hauptkonfigurationsdatei
# Änderungen mit Editor vornehmen z.B. nano 
cd /etc/httpd/conf/httpd.conf; nano httpd.conf 
# Danach Neustart oder Reload 
# Restart funktioniert immer
systemctl restart httpd 

## Schritt 4:
# Firewall freigeben 
# D.h. welche zone ist active -> public 
firewall-cmd --get-active-zones  
# konfigurieren 
firewall-cmd --add-service=http --permanent 
firewall-cmd --add-service=https --permanent 
firewall-cmd --reload 

## Schritt 5: 
# Mit Browser testen 

## Achtung: Optional, manchmal schiesst selinux quer 
# z.B. beim Ändern eines Ports 
# mit sestatus prüfen 

```

