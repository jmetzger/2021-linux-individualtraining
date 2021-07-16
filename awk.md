# awk 

## Examples

```
awk '{print $3 "\t" $4}' /etc/services 
awk '/tcp/' /etc/services 

awk '{print $2" "$1}' services
```



