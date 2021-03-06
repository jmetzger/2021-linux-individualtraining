# Linux Individual-Training

## Agenda 

  1. Distributionen 
     * [Überblick](overview-distros.md)
     * [Aufbau/Komponenten](aufbau.md)
  1. Verzeichnisse und Dateitypen 
     * [Verzeichnisaufbau](verzeichnisaufbau.md)
     * [Dateitypen](dateitypen.md) 
  1. Basisbefehle
     * [In den Root-Benutzer wechseln](sudo.md)  
     * [Wo bin ich ?](pwd.md)
     * [Praktische Ausgabe von langen Seiten - less](less.md) 
     * [Datei anlegen - touch](touch.md)
     * [Autovervollständen * und tab](autocomplete.md) 
     * [Welches Programm wird verwendet](which.md)
  1. Erweiterte Befehle (Nice to have) 
     * [Alias Befehle anzeigen](alias.md)
     * [Welche Bibliotheken verwendet ein ausführbares Programm](ldd.md)
     * [Wo liegt ein ausführbares Programm](which.md) 
  1. Dateien und Verzeichnisse
     * [Mit cd im System navigieren](cd.md)
     * [Verzeichnisse in Listenansicht mit versteckten Dateien anzeigen -> ls -la](list.md)
     * [Inhalt in Datei schreiben und anhängen](file-write-append.md)
     * [Verzeichnisse anlegen](mkdir.md)
     * [Verzeichnisse und Dateien löschen](file-dir-delete.md)
     * [Kopieren/Verschieben/Umbenennen von Dateien und Files](file-rename-copy-mv.md) 
     * [Grafisch Navigieren auf der Kommandozeile - mc](mc.md) 
  1. Systemadministration 
     * [Hostname setzen/abfragen](hostnamectl.md) 
     * [ssh absichern](ssh-absichern.md)
  1. Prozesse 
     * [Prozesse anzeigen - ps/pstree -p und top](prozesse.md)
  1. Benutzer, Gruppen und Rechte 
     * [Rechte](rechte.md) 
     * [Dateien für Benutzer und Gruppen](files-users-groups.md) 
     * [Benutzer anlegen](create-users.md) 
     * [Wie funktioniert die Maske (umask)](umask.md) 
     * [sudo Benutzer erstellen](mod-user-sudo.md) 
  1. Dateimanipulation/Unix Tools
     * [Anfang oder Ende einer Datei/Ausgabe anzeigen](head-tail.md)
     * [cat/head/tail-Beginn/Ende einer Datei anzeigen](cat-head.md)
     * [zcat - Inhalte einer mit gzip komprimierten Datei anzeigen](zcat.md)
     * [wc - Zeilen zählen](wc.md)
     * [Bestimmte Zeilen aus Datei anzeigen - grep](grep.md)
     * [Erweiterte Suche mit Grep](grep-extended.md)
     * [Find](find.md)
     * [sed](sed.md) 
     * [awk](awk.md)
  1. Logs/Loganalyse
     * [Logfile beobachten](tailf.md)
     * [Dienste debuggen](debug-service.md)
     * [Rsyslog](rsyslog.md)
  1. Variablen
     * [Setzen und verwenden von Variablen](variables.md) 
  1. Dienste/Runlevel(Targets verwalten) 
     * [Die wichtigsten systemctl/service](systemctl-service.md)
     * [Systemctl - timers](systemctl-timers.md)
     * [Gegenüberstellung service etc/init.d/ systemctl](service-initd-systemctl.md)
  1. Partitionierung und Filesystem
     * [parted and mkfs.ext4](parted-mkfs.md)
  1. Boot-Prozess und Kernel 
     * [Grub konfigurieren](grub.md)
     * [Kernel-Version anzeigen](kernel-version.md) 
     * [Kernel-Module laden/entladen/zeigen](kernel-modules.md) 
  1. Hilfe 
     * [Hilfe zu Befehlen](help.md)
  1. Grafische Oberfläche und Installation 
     * [Gnome unter Ubuntu installieren](gnome-ubuntu.md) 
     * [X-Server - Ausgabe auf Windows umleiten](xserver-windows-client.md)
     * [Installations-Images-Server](https://ubuntu.com/download/server#download) 
  1. Installation/Wartung und Aktualisierung
     * [Aktualisierung des Systems](update-upgrade.md)
     * [Paketmanager apt/dpkg](apt-dpkg.md) 
     * [Paketmanager rpm/yum](rpm-yum.md)
     * [Archive runterladen und entpacken](tar-download.md) 
     * [Lokalen Mirrorserver aufsetzen - Centos](https://wiki.centos.org/HowTos/CreateLocalMirror)
     * [Installationsbeispiel Apache auf Centos](install-apache.md)
  1. Firewall und ports
     * [ufw (uncomplicated firewall)](ufw.md)
     * [firewalld - Ubuntu](firewalld.md)
     * [firewalld - Centos 8](firewalld-centos8.md)
     * [Scannen und Überprüfen mit telnet/nmap](telnet-nmap.md) 
  1. Netzwerk/Dienste 
     * [IP-Adresse von DHCP-Server holen (quick-and-dirty)](dhclient.md) 
     * [IP-Adresse auslesen](ip-adresse-auslesen.md) 
     * [Netzwerk unter Centos konfigurieren - nmtui](nmtui.md)
     * [Netzwerk unter Centos konfigurieren - sysconfig](network-sysconfig.md)
     * [Auf welchen Ports lauscht mein Server](lsof.md) 
     * [Netzwerkabel drin/nicht drin?](netzwerkkarte-kabel-drin.md)
     * [Welcher DHCP-Server über NetworkManager](dhcp-server.md)
  1. Tools/Verschiedens 
     * [Remote Desktop für Linux / durch Teilnehmer getestet](https://wiki.ubuntuusers.de/Remmina/)
     * [Warum umask 002 und 0002 ? - Geschichte](umask-002-022-why.md)
     * [lokale Mails installieren](local-mail.md)
  1. Bash/Bash-Scripting 
     * [Einfaches Script zur Datumsausgabe](script-date.md) 
     * [Ausführen/Verketten von mehreren Befehlen](multiple-commands.md)
     * [Howto: Bash Scripting](https://tldp.org/LDP/Bash-Beginners-Guide/html/sect_02_02.html)
     * [Howto: Advanced Bash Scripting](https://tldp.org/LDP/abs/html/)
  1. Timers/cronjobs 
     * [Cronjob - hourly einrichten](cronjob-hourly.md)
     * [cronjob (zentral) - crond](crond.md)
     * [Beispiel-Regelmäßiges Scannen mit nmap](nmap-timer.md) 
  1. Literatur/Documentation 
     * [Literatur](literatur.md) 
     * [Linux Sicherheit/SELinux/nmap](https://schulung.t3isp.de/documents/linux-security.pdf)
     * [sssd gegen ADS](https://access.redhat.com/articles/3023951)
     * [realmd gegen ADS](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html-single/windows_integration_guide/index#sssd-ad-proc)
     * [MariaDB Galera Cluster mit Ansible](https://github.com/jmetzger/ansible-galera-cluster-maxscale)
     * [Ansible Module](https://docs.ansible.com/ansible/2.9/modules)
     * [Linux Hardening - TelekomSecurity](https://github.com/telekomsecurity/TelekomSecurity.Compliance.Framework)
     * [Example Question Linux Foundation LFCSA](https://training.linuxfoundation.org/wp-content/uploads/2019/04/LFCS-Practice-Questions-v1.0.pdf)
  
  1. Tipps&Tricks 
     * [Output von terminal sesssion inkl. SSH-Verbindung loggen](https://leszekjaskierny.wordpress.com/2017/01/27/mac-x-os-log-terminal-session-to-file/)
     * [Vagrant (Windows/OS X)](vagrant.md) 
     * [Centos auf Virtualbox installieren](centos-virtualbox.md) 
     * [Digitalocean - droplet-virtual machine installieren](https://www.digitalocean.com/)
     * [bash-profile testen](bash-profile.md)

  1. Übung 
     * [Übung Dateisystem](uebung-filesystem.md) 
     * [Übung Komplett - Centos8](uebung-komplett.md)

