- Use the output of grub-mkimage -V to check the GRUB version. It should be 2.02 so that the menu can chainload a boot loader built by elilo.
- Set the sound on if brltty is running when EFI3M runs, as with espeak and orca. This could help blind users using only a Braille device but no TTS application.