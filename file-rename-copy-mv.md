# File/Verzeichnis - rename/copy/mv 

## Dateien umbenennen, verschieben, kopieren 

```
# wenn Zeilverzeichnis nicht existiert -> Fehler ! 
cp -a todo.txt /dokumente/ 
# wenn zielverzeichnis nicht existiert, wird dokumente2 erstellt als file - > Achtung !! 
cp -a todo.txt /dokumente2 

# umbenennen
mv datei1 neuernamedatei1 

# verschieben in Verzeichnis 
mv datei1 /dokumente/
# besser als:
# mv datei1 /dokumente 
# weil hier die Datei dokumente angelegt wird, wenn der Ordner /dokumente nicht existiert !! 

```

## Ordner verschieben 

```
# Wir sind root 
cd /root
# Vorbereitung 
mkdir test 
cd test 
mkdir pruefung
cd pruefung
touch ergebnis 

# Verzeichnis training 
mkdir /root/training 

# Jetzt verschieben 
# Schritt 1: Ins Verzeichnis reinwechseln, dass Verzeichnis beinhaltet, dass ich verschieben möchte
cd /root/test
# Variante 1: mit absolutem Pfad 
mv pruefung /root/training
# Alternativ: Variante 2: relativier Pfad
mv pruefung ../training 

```

## Rechte behalten bei kopieren

```
# -a macht das 
cp -a todo.txt todoneu.txt 

# ohne -a werden symbolische links aufgelöst und die Rechte des ausführenden Nutzers gesetzt
cp ab cd 

# Verzeichnisse kopieren
cp -a /etc /etc3

```
