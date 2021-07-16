# sed 

## Examples 

```
# Search for all occurences of tcp 
cp /etc/services /root/services 
cd /root 
sed 's/tcp/linux/g' geekfile.txt

# line 1 to line 3 
sed '1,3 s/unix/linux/' geekfile.txt

```

## Delete 



## Delete Pattern matching line 

```
sed '/pattern/d' filename.txt
```


## Ref

  * https://www.geeksforgeeks.org/sed-command-in-linux-unix-with-examples/
