# EFI3M
EFI Multi-boot Menu Maker 

EFI3M builds a Multi-boot menu for computers with an EFI firmware.

The menu will be displayed when booting the computer and allows the user to start any of the installed system from its EFI boot loader: not only Linux distributions, but also BSD distributions, Microsoft Windows, Apple OS X, pretty much any system that has a boot loader in an ESP (EFI System Partition) on any drive of the computer, be it a hard disk, a SSD, a NVMe, whatever.

The multi boot menu is installed in an internal ESP as /EFI/efibootmenu/BOOTx64.EFI alongside its configuration file grub.cfg and also, optionally, in /EFI/BOOT/ which is the fall back directory looked at by the firmware, if it is not not already busy.

It can also be installed on an USB stick, to allow booting any installed system if for some reason booting would otherwise fail.

The main menu of EFI3M is presented below:

```
*** EFI multiboot menu maker ***
	
Available features:
1 Build and install the multiboot menu on your computer
2 Make a rescue USB stick providing the boot menu
3 Customize the boot menu
4 Information about EFI3M

Just press Enter to quit.

Your choice: 
```
Here is the Customize sub-menu:

```
Current menu (custom labels on the second line):

1  (sda1)/EFI/Slint/elilo.efi
   Label: Slint 14.2.1.1
2  (sda1)/EFI/Slint/grubx64.efi (hidden)
3  (sde1)/EFI/Slackware/elilo.efi
   Label: Slackware 14.2
4  (sdb2)/EFI/Microsoft/Boot/bootmgfw.efi
   Label: Windows 10
5  (nvme0n1p1)/EFI/opensuse/grubx64.efi
   Label: openSUSE 15.0 Leap
6  (nvme0n1p1)/EFI/ubuntu/fwupx64.efi (hidden)
7 (nvme0n1p1)/EFI/ubuntu/grubx64.efi
   Label: GRUB from Ubuntu 18.05
8 (nvme0n1p1)/EFI/ubuntu/shimx64.efi (hidden)
9 (nvme0n1p1)/EFI/ubuntu/mmx64.efi (hidden)
   Label: MoK Manager from Ubuntu
10 (sdc1)/EFI/fedora/MokManager.efi
11 (sdc1)/EFI/fedora/gcdx64.efi
   Label: GRUB menu from Fedora 28

Type:
a number between 1 and 11 to select a boot entry then set
  the label used to display it in the boot menu,
D to set the Delay before auto boot,
M for a Mute menu, S for a menu with Sound,
O to modify the boot Order,
V to Validate your modifications.

Just press Enter to undo all modifications and return to the main menu.

Your choice:
```

As shown EFI3M also allows the user to easily customize the boot menu, modifying the label of a boot entry (how it is displayed), hiding it, reordering the boot entries, setting the delay before auto boot.

To help the visually impaired, the boot menu optionally plays a sound at startup, a tune of n sounds when starting
the boot entry number n, and specific tunes for reboot and halt.

EFI3M has been tested on Slint, Slackware, Salix, Debian, Ubuntu, Fedora, openSUSE and Arch.

It should run in any Linux system including GRUB (I mean GRUB2).

For questions or issues, send en email to the author:
didier~at~slint~dot~fr.

Didier Spaier
