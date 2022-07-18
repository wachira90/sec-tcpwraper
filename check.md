# check supprt

````
for file in /usr/sbin/*
do
    ldd $file 2>/dev/null | grep -q libwrap.so && echo $file
done
````

## result 

````
/usr/sbin/gdm3
/usr/sbin/sshd
/usr/sbin/tcpd
/usr/sbin/tcpdchk
/usr/sbin/tcpdmatch
/usr/sbin/try-from
````

## check command

````
root@test-imac:~# ldd $(which sshd) | grep libwrap
        libwrap.so.0 => /lib/x86_64-linux-gnu/libwrap.so.0 (0x00007fa3dbd93000)
root@test-imac:~#
````
