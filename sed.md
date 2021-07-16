# sed 

## Examples 

```
# Search for all occurences of tcp 
cp /etc/services /root/services 
cd /root 
sed 's/tcp/linux/g' services

# line 1 to line 3 
sed '1,3 s/unix/linux/' services 

```

## Delete 



## Delete Pattern matching line 

```
# Example 1
cd /root
sed '/tcp/d' services

# Example 2 
cd /root
sed '/^#/d' services > services_no_comments


```


## Edit in place 

```
sed '/^#/d' -i.bkup services


```

## Ref

  * https://www.geeksforgeeks.org/sed-command-in-linux-unix-with-examples/
