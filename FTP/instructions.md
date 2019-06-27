# FTP

1. Install vsftpd

```
sudo apt install vsftpd
```

2. Open file /etc/vsftpd.conf

```
sudo vim /etc/vsftpd.conf 
```

3. Change the follow lines

```
anonymous_enable=NO
...
#write_enable=YES
...
#chroot_local_user=YES
```

to

```
anonymous_enable=YES
...
write_enable=YES
...
chroot_local_user=YES
allow_writeable_chroot=YES
```

4. Restart the server
```
sudo service vsftpd restart
```