=================================
QUEEN K JUUL's LCARS 7.10 UTILITY
=================================

Lots of 
Convenient
Accessories for
Retro
Systems

Based on "MS-DOS 7.10," the custom repack of 9x DOS by the China DOS Union

Designed to be able to install Windows 9x on a machine with USB ports but 
no functional CDROM, though I imagine it could be useful in other situations. 

_________
UTILITIES
---------


[SHSUCD] - Virtual CDROM Device Manager
---------------------------------------

    Mounts a CDROM image (ISO, BIN) to the next available drive letter. For 
    your convenience, a frontend script is provided to simplify mounting, 
    though full features are installed 
    (see http://adoxa.altervista.org/shsucdx/index.html)

    USAGE:  mount <PATH_TO_IMAGE>       // mounts disk to next available letter
            umount                      //unmounts all mounted image files

[SHSUFDRV] - Virtual Floppy Device Manager
------------------------------------------

    Mounts a floppy disk image (IMG) to next available drive letter. The alias 
    FMOUNT is used on this system, thoguh the standard SHSUFDRV utilities are 
    installed (see http://adoxa.altervista.org/shsufdrv/index.html)

    USAGE: fmount /F:<PATH_TO_IMG>      // mounts disk to next available letter
           fmount /u                    // unmounts all mounted disk images

[USBASPI] - Universal USB Drivers for DOS
-----------------------------------------

    Installed to CONFIG.SYS. Scans USB controllers on boot, and mounts any 
    detected FAT32 USB Mass Storage devices. Can be picky about drives. 
    MBR only, FAT16 or FAT32 only. Anecdotally, it's best to have your 
    drive freshly formatted on a Windows machine 
    (Linux partition + format tools don't always work). 

[PKZIP / PKUNZIP] - ZIP Codec
-----------------------------

    Classic and self-explanatory. Baked right in. 

[RAMDRIVE] - RAM Disk Installation
----------------------------------

    Can be used to install contents of the floppy to RAM, to free up the drive
    for another disk. I haven't automated this process yet. It will require 
    modifying CONFIG.SYS. File is included, but you're on your own to find 
    instructions online at the moment. 

[CHKDSK] - DOS Disk Check Utility
[SCANDISK] - Windows 95 Disk Check Utility
[FORMAT] - Disk Format Utility
[FDISK] - Disk Partition Utility
[XCOPY] - Bulk Copy / Backup Utility
----------------------------

    Classic DOS Disk Utilities, included. 

[EDIT.COM] - Text Editor
------------------------

    Classic DOS text editor, included. 



________
FEATURES
--------

[NIXINESS] - `ls` can be run in place of `dir /o /w'. DOSKEY and MORE installed
     for tab completion, command history, and useable output. 
     MORE is also aliased to LESS

[CDROM] - Includes both OAKCDROM.SYS and VIDE-CDD.SYS

[DOSLFN] - DOS / Win9x Long Filename support

[FAT32] - FAT32 disk support

[HIMEM / EMM386] - Configured out of the box for high memory support to 
    nable RAMDISKS or CD-ROM software

[NTFS] - Read-only NTFS drives are mounted automatically at boot

___________________
-------------------

This is very much DOS for "modern" machines (Pentium and above). No 
consideration was given to memory conservation, and the included utilities are 
only really useful if you have storage large enough to handle collections of 
disk images, USB accessories, and existing Windows installations. It presumes
that EMS and XMS are available, and it works best when installed to a RAMdrive.

My original use case was a Pentium 233 laptop with a dead CDROM, but working
FDD and USB ports. Win95 ISO goes on the USB, mount it as virtual CDROM, 
copy the contents to HDD, run Setup from there. Remarkably, ALL the utilities
I find essential to a modern DOS getup-zip tools, shsucd/shsufd, LFN, NTFS, etc
fit on a single 1.44--which I honestly found very surprising. 