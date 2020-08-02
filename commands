#### Creating partitions
to see partition in disk
cat /proc/partitions  (here sdb don't have any nely partitions
fdisk /dev/sdb
m --print the menu
p for printing sector info
n for new partitions 


you will get options

partion number   (you may select default)
first sector  (you may use default)
last sector              (if you use enter will use the entire disk) option is +size{K,M,G,T,P} you may use sth like +100M

p to check what changes you made and w will write to disk

if you get some error like Device or resource busy, just reboot.

#### creating filesystem
mkfs 
mkfs.xfs --help

label is like name for file system

mkfs.xfs -L myfs /dev/sdb1

#### mounting to use the filesystem
mount /dev/sdb1 /mnt
mount | grep ^/dev
umount /mnt or umount /dev/sdb1

device name can change so mount won't work, you can so use uuid. 


ctrl + r (search back in history) and ctrl + r to specify different similar patterns from history

#### mount automatically using /etc/fstab
/dev/mapper/rhel-root /  xfs  defaults 1 1
UUID=343df-234df3-dsf-23423   /boot xfs defaults  1 2
LABEL=myfs    /data   xfs defaults   1 2                    (last column is fsck, for root 1, for other 2)


mkdir /data
mount -a
verify by mount | grep ^/dev/


use LABEL and UUID instead of device name

xfs_admin -L bootdevice /dev/sdb1
now blkid 

