# Arch-install-note

Quick note to Arch Linux Disotro

----

## Installation

### Partition 

gdisk /dev/sda

LABEL SIZE CODE NAME
BOOT 1GB EF00 EFI system partition
ROOT Rest 8300 Linux File System

Number 	Type 	Size
1 	EFI 	512 Mb
2 	Linux Filesystem 	99.5Gb (all of the remaining space )

### Format 




=====

## Issues:

### Boot Loader Alert
⚠️ Mount point '/boot' which backs the random seed file is world accessible, which is a security hole! ⚠️
⚠️ Random seed file '/boot/loader/.#bootctlrandom-seed25**************' is world accessible, which is a security hole! ⚠️

Solution: Change /etc/fstab /boot (/EFI) fmask=0077, dmask=0077 


### Ambient Sensor not working

'https://github.com/mikhail-m1/illuminanced'


### DBeaver JDK Version 17+ 

"archlinux-java status"

"# archlinux-java set <JAVA_ENV_NAME>"

### USB HDD has No Write Access

 -Environment: KDE(Plasma) 
 
 -Mounted USB HDD fs: Btrfs
 
 Solution: Chmod 777 /run/media/[User ID]/[Mounted Device ID]

 
