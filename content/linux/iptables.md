+++
title = "iptables"
weight = 5
date = "2016-11-06T00:17:50+02:00"

+++

#### List all active iptables rulese by specification

```
iptables -S
```

#### Add a simple rule

```
iptables -A INPUT -m state --state NEW,ESTABLISHED,RELATED -j ACCEPT
```

#### Save the rules
```
/sbin/service iptables save
```
