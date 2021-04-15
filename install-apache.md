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
```

## Apache started nicht wg Port-Änderung (Port: 82)  - Quick and Dirty Lösung

```
# Es kommt ein Fehler bei Apache port 82 (Listen 82) 
systemctl start httpd

# Schritt 1: Prüfen, ob selinux aktiv ist
sestatus # Sucht 2 Einträgen enforcing 

# Schritt 2: selinux testweise abschalten 
setenforce 0 # das heisst, regeln werden protokolliert, aber nicht durchgesetzt 

# Schritt3: 
systemctl restart httpd 

# Wenn das der Fall ist, selinux deaktivieren 
/etc/selinux/config 
# mit editor 
SELINUX=permissive
# oder wenn man generell selinux nicht einsetzten möchte:
SELINUX=disabled 
# Danach rebooten 
```

## Apache started nicht wg Port-Änderung (Port: 82)  - Nice and Smooth (better!) 

```
semanage port -a -t http_port_t -p tcp 82 
setenforce 1 
systemctl restart httpd 
```
