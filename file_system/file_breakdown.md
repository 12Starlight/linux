# **File System**

&nbsp;

| **Directory** | **Purpose**                                                               |
|--------|-----------------------------------------------------------------------------------|
| /      | The Very Top (Root) of The File Tree. Holds Everything else.       |
| /bin   | Stores Common Linux user command `bin`aries. e.g date, cat, cal commands are here. |
| /boot  | Bootable linux Kernal and bootloader config files.
| /dev   | Files representing `dev`ices. tty=terminal, fd=floppydisk, (sd or hd)=harddisks, ram=RAM, cd=CD-ROM. |
| /etc   | Administrative Configuration files. The format for many of these configurations can be found in section 5 of the Linux Manual. |
| /home  | Where the home directories for regular users are stored. For example, mine is at /home/dave. |
| /media | Unlike /dev, /media is usually where removable media (USB sticks, external hard drives etc.) are mounted. |
| /lib   | Contains `lib`raries needed by applications in /bin and /sbin to boot the system. |
| /mnt   | A place to mount external devices. This can still be used, but has been superseded by /media. |
| /misc  | A directory used to sometimes automount filesystems on request. |
| /opt   | Directory Structure used to store additional (i.e. `opt`ional) software. |
| /proc  | Information about System Resources. |
| /root  | The home folder for the root user aka the superuser (similar to the administrator on Windows). |
| /sbin  | Contains administrative commands (`bin`aries) for the root (`s`uper) user. |
| /tmp   | Contains `temp`orary files used by running applications. |
| /usr   | Contains files pertaining to users that in theory do not change after installation. |
| /var   | Contains directories of `var`iable data that could be used by various applications. System log files are usually found here. | 