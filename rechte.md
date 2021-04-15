# Rechte 

## Arten 

```
r = Lesen 
w = Schreiben
x = Ausführen 
```

## Aufbau triple 

```
kurs@ubuntu2004-101:~$ # rwx | rw- | r--
kurs@ubuntu2004-101:~$ #  u    g      o
kurs@ubuntu2004-101:~$ # 421 | 42- | 4--
kurs@ubuntu2004-101:~$ #  7  |  6  | 4

# rwx | rw- | r--
#  u    g      o
# 421 | 42- | 4--
#  7  |  6  | 4
```

## Berechtigungen mit Symbolen setzen 

```
chmod g+w,o+r testfile
```

## Ausführungsrechte für Benutzer für Script setzen

```
chmod u+x script.sh 
```

## SGID - Bit setzen 

```
# Alle neuen Dateien und Verzeichnisse bekommen als Gruppe die Gruppe des Verzeichnisses
ls -la | grep dokumente
drwxrwsr-x.   5 root dg4   131 15. Apr 10:18 dokumente

# d.h. hier sind neu angelegte Ordner und Dateien in der Gruppe 'dg4'
# Abweichend vom Standardverhalten: user/gruppe vom benutzer der Datei anlegt 

# + Vererbung funktioniert hier auch. 


chmod g+s /dokumente 
```
