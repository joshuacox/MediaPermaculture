# MultiBooting

This is the process of getting your machine to boot more than one operating system.  This is most commnoly used when purchasing a new machine, wherein you want to install Linux and preserve the lame OS that the computer came with.

First, before anything else you should attempt to get a capture of the computer in it's raw state.  Before it is initialized the first time where it asks you to setup your user etc.

If you do this you can sell the computer at a later date and reinitialize it to the exact state as when you bought it.

To do this in most cases you are going to have to acess the BIOS before the machine boots the hard disk for the first time.  It is easiest if you actually remove the drive at this time and merely copy it using another machine.  But let's assume you can't do that.  To access the bios of your machine you will need to hit the 'setup' key for your computer during boot, this is different depending the exact machine you have, but it is usually F2, or delete, or F1, or F10, or F11, or F12, really someone should have made a standard 40 years ago, but instead they just left it to be willy niilly.  Forum posts [here](http://askubuntu.com/questions/180244/how-do-i-enter-bios) and [UEFI](https://www.linux.com/learn/how-install-linux-windows-machine-uefi-secure-boot) brings its own [issues](https://help.ubuntu.com/community/UEFI).  Once you do get into the BIOS you need to tell the machine to boot from a USB drive loaded with this..

### [Clonezilla](http://clonezilla.org)

> Clonezilla is a partition and disk imaging/cloning program similar to True Image® or Norton Ghost®. It helps you to do system deployment, bare metal backup and recovery. Two types of Clonezilla are available, Clonezilla live and Clonezilla SE (server edition). Clonezilla live is suitable for single machine backup and restore. While Clonezilla SE is for massive deployment, it can clone many (40 plus!) computers simultaneously. Clonezilla saves and restores only used blocks in the hard disk. This increases the clone efficiency. With some high-end hardware in a 42-node cluster, a multicast restoring at rate 8 GB/min was reported.

Once you've got clonezilla booted you will notice it has the ugliest UI ever, this is a good thing.  Instead of wasting time changing the user interface they have made the best backup program on the planet.  And because of this you will only have to learn once and you'll be able to backup machines at a very lowlevel for the rest of your life.

Once you have made a clone of the machine, you are ready to shrink the main partition.  You can do this easily from the installer of Linux Mint, Ubuntu, Debian, or Fedora, or you can do it beforehand by booting a USB copy of:

### [SysRescueCD](http://www.system-rescue-cd.org/)

> SystemRescueCd is a Linux system rescue disk available as a bootable CD-ROM or USB stick for administrating or repairing your system and data after a crash. It aims to provide an easy way to carry out admin tasks on your computer, such as creating and editing the hard disk partitions. It comes with a lot of linux software such as system tools (parted, partimage, fstools, ...) and basic tools (editors, midnight commander, network tools). It can be used for both Linux and windows computers, and on desktops as well as servers. This rescue system requires no installation as it can be booted from a CD/DVD drive or USB stick, but it can be installed on the hard disk if you wish. The kernel supports all important file systems (ext2/ext3/ext4, reiserfs, btrfs, xfs, jfs, vfat, ntfs), as well as network filesystems (samba and nfs)


There you can pull up:

###### [GpartED](http://gparted.org/) 

> GParted is a free partition editor for graphically managing your disk partitions.
> With GParted you can resize, copy, and move partitions without data loss, enabling you to:
> *  Grow or shrink your C: drive
> *  Create space for new operating systems
> *  Attempt data rescue from lost partitions

Shrink the largest partition down to give yourself some new space to install linux to.

Now, proceed to booting off of thumb drive copy of one of the Linux distrubutions





