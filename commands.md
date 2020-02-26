#### Creating partitions

cat /proc/partitions
fdisk /dev/sdb
m --print the menu
p for printing sector info
n for new partitions 


you will get options

partion number   (you may select default)
first sector  if given sth like (34-257) you can use first index number here its 34
last sector              (if you use enter will use the entire disk) option is +size{K,M,G,T,P} you may use sth like +100M

p to check what changes you made and w will write to disk

if you get some error like Device or resource busy, just reboot.

#### creating filesystem
mkfs 
mkfs.xfs --help

label is like name for file system

mkfs.xfs -L myfs /dev/sdb1
