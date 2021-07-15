# Prozesse 

## Prozesse anzeigen 

```
ps -ef 
ps aux  # x alle Prozesse anzeigen, die nicht an ein Terminal gebunden sind 
```

## Prozesse anzeigen für Benutzer 

```
ps -u kurs -o pid,cmd # -o für felder der ausgabe 
```

## Wieviele apache - Prozesse gibt es ? 

```
# Achtung Ergebnis - 1 - weil grep noch mit auftaucht
ps aux | grep -c apache 
```

## top für bestimmten user 

```
top -U kurs 
```

## systemctl (läuft Dienst) 

```
systemctl status sshd 

```

## Prozeßbaum anzeigen (meist nicht für die Praxis notwendig) 

```
pstree -p 
```
