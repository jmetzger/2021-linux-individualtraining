# Dateien anzeigen / Teile davon 

### cat mit Zeilennumer 

```
cat -n /etc/services 
```

### Die ersten -x Zeilen anzeigen 

```
# ersten 10 Zeilen anzeigen
head /etc/services 

# Ersten 20 Zeilen 
head -n 20 /etc/services  
```

## Die letzten -x Zeilen anzeigen 

```
# die letzten 10 Zeilen 
tail /etc/services 

# die letzten 40 Zeilen 
tail -n 40 /etc/services

cat /etc/services | tail -n 500
# mit umleitung datei 
cat /etc/services | tail -n 500 >> neuedatei # anhängen - bestehende Zeilen werden nicht überschrieben.
```

## Ausgabe der letzten Zeilen und ausgabe in Datei 

```
cd /var/log 
tail -n 100 syslog.1 >> fehlerlog 
cat fehlerlog
```
