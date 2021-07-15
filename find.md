# Find 

## Simple find command 

```
# find directories with specific name 
find / -name tmpfiles.d -type d 
```

## Find diretories ending on ".d" 

```
find / -type d  -name "*.d"
```

## Find files by inode and delete them 

```
# helpful when file name is cryptic
# see what the inode with 
# ls -lai # -i for inode number 
find -inum 12604361 -type f -delete
```
