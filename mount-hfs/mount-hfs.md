
# Mount USB drive in HFS+
```
sudo apt-get install hfsprogs
sudo mount -t hfsplus -o force,rw /dev/sdc2 /media/larzdata
```

vi /etc/fstab
```
# <file system> <mount point>   <type>  <options>       <dump>  <pass>
/dev/sdc2 /media/larzdata hfsplus force,rw,nobootwait 0 0
```

# How do I avoid the “S to Skip” message on boot?
http://askubuntu.com/questions/120/how-do-i-avoid-the-s-to-skip-message-on-boot
Option `nobootwait`

