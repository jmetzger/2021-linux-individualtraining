# Übung komplett (Centos 8/Redhat 8)  

```
Erstelle den Nutzer "teilnehmer" 
Setze ein Passwort für den Nutzer
Sorge dafür, dass der Nutzer als "root" arbeiten kann
Test dies mit einer neuen ssh-Verbindung (Putty) 
Erstelle eine neue Gruppe teamwork 
Ornder teilnehmer dieser Gruppe zu. 

Erstelle eine neue Verzeichnisstruktur im Heimatverzeichnis von "teilnehmer" -> planung/themen/projekte
Kopiere die Datei /etc/services in den neue angelegten Unterordner projekt
Lass die ersten 1000 Zeilen der services datei in projekte ausgeben und schreibe diese in ergebnis_ports
Lass die letzten 500 Zeilen der services datei in projekte ausgeben und hänge diese ans Ende von ergebnis_ports an
Zählen die Zeilen in ergebnis_ports in denen am Anfang der Zeile ein Kommentar vorkommt und schreibe das Ergebnis in ergebnis_ports_anzahl 
Zähle alle Zeilen in ergebnis_ports und zwar nicht mit grep und hänge das Ergebnis in ergebnis_ports_anzahl an.

Installiere mariadb-server
Finde heraus, wie der Dienst heisst (Hinweis: der mit dem @-Zeichen ist es nicht)
prüfe ob der Dienst nach läuft, starte den Dienst und aktiviere ihn (enable)
Find heraus, ob der Dienst nach aussen lauscht (port offen) 

Finde heraus unter welchen Prozess-ID's (1 oder mehrere) der mariadb-server läuft

```
