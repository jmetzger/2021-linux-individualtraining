# Enable sudo for user 

## Benutzer zum Sudo benutzer machen (Ubuntu/Debian) 

```
adduser newuser
usermod -aG sudo newuser
## testing 
su - newuser
groups # see if we are in groups sudo 
id # shows the same but more info 
# need to enter password here 
sudo su -
```

## Benutzer zum sudo benutzer machen (Redhat/Centos) 

```
adduser newuser
usermod -aG wheel newuser
## testing 
su - newuser
groups # see if we are in groups sudo 
id # shows the same but more info 
# need to enter password here 
sudo su -
```
