+++
weight = 5
toc = true
date = "2016-11-19T16:02:39+02:00"
title = "Hostname rename"
+++

Edit the hostname in /etc/hostname using a text editor
```
sudo vim /etc/hostname
``` 

Delete the the old name and setup new. Save the file
Next edit the hosts file:

```
sudo vim /etc/hosts
``` 

Replace all occurances of the old hostname with the new and save the file.

Finally reboot:

```
sudo reboot
```  
