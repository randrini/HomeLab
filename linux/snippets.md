*Search for a string in all directories*

  `nice -19 grep -airlE 'net.ipv4.ip_forward|/proc/sys/net/ipv4/ip_forward' / `
  
  `grep -rn net.ipv4.ip_forward /etc/*`

*SFP to another linux and copy file*
```shell
sftp root@192.168.1.100
get filename
get -r recursiveFolder/
````

Copy over SSH 

$ cd Documents
Connect

$ sftp sammy@your_server_ip_or_remote_hostname
Go the directory that contains the file to be transferred.

$ cd NASA/secret_files/
Transfer

$ get UFO_blueprint.odt
To get the complete directory, instead use

$ get -r secret_files/
