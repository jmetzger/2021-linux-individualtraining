# Die Maske, die Maske (umask) 

## Welche Rechte haben neue Dateien 

  * Diese wird durch die Maske des eingeloggten Benutzers bestimmt (umask)

## Maske anzeigen / setzen

```
umask 

# Nur während der Session aktiv
umask 0222 
```

## Wie funktioniert es ? 

```
# Maximale Rechte einer Datei 
666 = rw-rw-rw-

# Maximale Rechte Verzeichnis 
777 = rwxrwxrwx

# Beim Anlegen eines Verzeichnisse / Datei werden die Rechte berechnet:

# Datei 
  0666
- 0002 <- diese Wert kommt von umask 
======
  0664 <- Diese Rechte werden verwendet

# Verzeichnis 
  0777
- 0002 <- diese Wert kommt von umask 
======
  0775 <- Diese Rechte werden verwendet

```
