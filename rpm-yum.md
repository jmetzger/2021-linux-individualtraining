# Paketmanager rpm/yum 

## Wo werden die Repos konfiguriert 

```
/etc/yum.repos.d

```

## Grundbefehle 

```
# Was ist installiert
yum list --installed

# Nach Paket suchen 
yum search httpd 

# Paket installieren 
yum install httpd 

# Welches Installations-Paket stellt nmap zur Verfügung 
yum provides nmap 

```

## System aktualisieren / updaten 

```
# Installation updaten 
yum upgrade # yum update is still available but not documented 
## automatisch fragen bejahen 
yum -y update 

```

## Welche Paket stellt einen bestimmten Befehl zur Verfügung ? 

```
yum whatprovides sealert 
```

## Paket deinstallieren 

```
yum remove mariadb-server 
```
