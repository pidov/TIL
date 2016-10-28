# iptables 

List all active iptables rulese by specification
```
iptablese -S
``` 

Add a simple rule

``` 
iptables -A INPUT -m state --state NEW,ESTABLISHED,RELATED -j ACCEPT
```

Save the rules 
```
# /sbin/service iptables save 
```




