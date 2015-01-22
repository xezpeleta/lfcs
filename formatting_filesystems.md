# Formatting filesystems

* $ fdisk /dev/sdb
* $ gdisk /dev/sdb
* $ ls /sbin/mk*
* $ mkfs -t [filesystem] -L [label] device
* $ mkfs.[filesystem] -L [label] device
* etc/fstab /dev/sdX1 swap swap sw 0 0
* $ mkswap /dev/sdX1
* $ swapon -v /dev/sdX1
* $ cat /proc/swaps
* $ swapoff /dev/sdX1 (disable swap)
* 