# EFI3M
EFI Multi-boot Menu Maker 

EFI3M builds a Multi-boot menu for computers with an EFI firmware.

The menu will be displayed when booting the computer and allows the user to start any of the installed system from its EFI boot loader: not only Linux distributions, but also BSD distributions, Microsoft Windows, Apple OS X, pretty much any system that has a boot loader in an ESP (EFI System Partition) on any drive of the computer, be it a hard disk, a SSD, a NVMe, whatever.

The multi boot menu is installed in an internal ESP as /EFI/efibootmenu/BOOTx64.EFI alongside its configuration file grub.cfg and also, optionally, in /EFI/BOOT/ which is the fall back directory looked at by the firmware, if it is not not already busy.

It can also be installed on an USB stick, to allow booting any installed system if for some reason booting would otherwise fail.

The main menu of EFI3M is presented below:

```
EFI multiboot menu maker (EFI3M)

Available features:
1 Display features and usage
2 Install the multiboot menu on your computer
3 Make a rescue USB stick providing the boot menu
4 Customize the boot menu
5 Display the boot menu

Just press Enter to quit.

Type the number in front of the chosen feature:
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
7  (nvme0n1p1)/EFI/ubuntu/grubx64.efi
   Label: GRUB from Ubuntu 18.05
8  (nvme0n1p1)/EFI/ubuntu/shimx64.efi (hidden)
9  (nvme0n1p1)/EFI/ubuntu/mmx64.efi (hidden)
   Label: MoK Manager from Ubuntu
10 (sdc1)/EFI/fedora/MokManager.efi
11 (sdc1)/EFI/fedora/gcdx64.efi
   Label: GRUB menu from Fedora 28

Type either:
the number of a boot entry to customize its label,
D to set the Delay before auto boot,
M for a Mute menu, S for a menu with Sound,
O to modify the boot Order,
V to Validate your modifications.
Just press Enter to undo all modifications and return to the main menu.

Type the number or letter that corresponds to your choice.

```

As shown EFI3M also allows the user to easily customize the boot menu, modifying the label of a boot entry (how it is displayed), hiding it, reordering the boot entries, setting the delay before auto boot.

To help the visually impaired, the boot menu optionally plays a sound at startup, a tune of n sounds when starting
the boot entry number n, and specific tunes for reboot and halt.

EFI3M has been tested on Slint, Slackware, Salix, Debian, Ubuntu, Fedora, openSUSE and Arch.

It should run in any Linux system including grub version at least 2.02 with x86_64.efi modules and efibootmgr

If yu installed one of the predecessors of EFI3M, possibly named efimenu, remove the files it installed running the script remove_efibootmenu before running EFI3M.

For questions or issues, send en email to the author:
didier~at~slint~dot~fr.
or file an issue.

Didier Spaier
