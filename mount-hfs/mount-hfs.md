
# Mount USB drive in HFS+
```
sudo apt-get install hfsprogs
sudo mount -t hfsplus -o force,rw /dev/sdc2 /media/larzdata
```

vi /etc/fstab
```
# <file system> <mount point>   <type>  <options>       <dump>  <pass>
/dev/sdc2 /media/larzdata hfsplus force,rw 0 0
```
