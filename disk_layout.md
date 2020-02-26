#### when working with hard disk you need to know how to organize hard disk.
  * with Partitions
    * should decide before hand how much you want to allocate
  * with LVM
    * you are going to use one partion
    * create a physical volume
    * create a volume group
    * create a logical volume from volume group
 
 #### After creating partition, you have to create a file system
   * File System Differences (for Red Hat)
     * XFS
     * Ext4
     * Btrfs
     * vfat
     * GFS2
     * Gluster
 
#### XFS
  * Default file System in RHEL 7, but also  in other recent Linux distribution
  * Based on B-tree database ( database that is used to allocate disk space )

#### Ext4
  * It is used by RHEL 6
  * problem with Ext4 is that it is based on the 1993 ext2 File System (coz the storage need at that time and now are not similar)
  * It uses H-tree indexing (which might be slow)

####  Btrfs
  * Future promise
  * Copy-on-write(CoW) file system
    * Makes journing unnecessary
    
 #### vfat
   * for compatibility with other OS
   * useful for removable media
   
 #### GFS2
   * For Active/Active HA cluster environment
   
 #### Gluster
   * Distributed FS
   * Storage is in "Bricks" which uses XFS.
   
