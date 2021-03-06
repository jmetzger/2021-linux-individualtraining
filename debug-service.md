# Debug Service 

## Prerequisites 

```
# Install mariadb-server - Centos  
yum install mariadb-server 

# Find out the service name 
systemctl list-unit-files -t service | grep mariadb 

# 

```

## Walkthrough 

```
# Dienst startet nicht / nach Ausführen von systemctl restart wird Fehlermeldung ausgegeben
systemctl restart mariadb.service 

# Schritt 1 : status -> was sagen die logs (letzte 10 Zeilen) 
systemctl status mariadb.service 

# Nicht fündig-> Schritt 2:
jourrnalctl -xe

# Nicht fündig -> Schritt 3:
journalctl -u mariadb.service 

# Nicht fündig -> Schritt 4:
# Spezifisches Log von Dienst suchen 
#
# z.B. 
# grep -ir mariadb /var/log 
# und evtl. LogLevel von Dienst hochsetzen
#
# ODER: 
# z.B. bei mariadb (durch Internetrecherche herausfinden) 
less /var/log/mysql/error.log 

# Nicht fündig -> Schritt 5
# Allgemeines Log
# Debian/Ubuntu 
/var/log/syslog
# REdhat/Centos 
/var/log/messages 
```

## Falsche Option in welcher Konfigurationsdatei 

```
# wir haben die falsche Option gummitulpe drin 
grep -ir gummitulpe /etc 
```

## Wie verfahren bei SystemV 

```
Wie bei walkthrough aber ab Schritt 4
```

## Find error in logs quickly

```
cd /var/log/mysql 
# -i = case insensitive // egal ob gross- oder kleingeschrieben
cat error.log | grep -i error
```

