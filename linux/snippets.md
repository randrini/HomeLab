*Search for a string in all directories*

  `nice -19 grep -airlE 'net.ipv4.ip_forward|/proc/sys/net/ipv4/ip_forward' / `
  
  `grep -rn net.ipv4.ip_forward /etc/*`

*SFP to another linux and copy file*
```shell
sftp root@192.168.1.100
get filename
get -r recursiveFolder/
````
