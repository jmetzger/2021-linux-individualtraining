# Paketmanager rpm/yum 

## Wo werden die Repos konfiguriert 

```
/etc/yum/repos.d

```

## Grundbefehle 

```
# Was ist installiert
yum list installed

# Nach Paket suchen 
yum search httpd 

# Paket installieren 
yum install httpd 

# Installation updaten 
yum update 
## automatisch fragen bejahen 
yum -y update 

```
