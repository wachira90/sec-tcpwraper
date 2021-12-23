# security tcpwraper

## CHECK-MOD
````
ldd /sbin/sshd | grep libwrap

libwrap.so.0 => /lib64/libwrap.so.0 (0x00007f1fea580000)
````

## SYNTAX  `daemon_list : client_list [: command]`
````
daemon_list: => A comma-separated list of daemons, or keyword ALL for all daemons

client_list: => A comma-separated list of clients, or keyword ALL for all clients

command: => An optional command that is executed when a client tries to access a server daemon
````


## vi /etc/hosts.allow
````
sshd:192.168.1.2:allow
````


## vi /etc/hosts.allow
````
vsftpd : 192.168.2.*
````


## vi /etc/hosts.allow
````
sshd : ALL
````


## vi /etc/hosts.deny
````
vsftpd : ALL
````


## vi /etc/hosts.allow
````
vsftpd : .example.com
````

## vi /etc/hosts.deny
````
ALL: ALL EXCEPT 192.168.0.2
````

## vi /etc/hosts.deny
````
sshd : ALL EXCEPT 192.168.4.0/24 [fd00::]/64
````
