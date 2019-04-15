UDOO BOLT is supplied with a [American Megatrends International LLC(AMI)](https://ami.com/en/products/) BIOS/UEFI Firmware.

It is possible to access to AMI Setup Utility by pressing the escape key (`ESC`) after System power up, during POST phase.

## UEFI Update utility

At the following link you can find the latest BIOS/UEFI Firmware and the BIOS/UEFI Update Utility to quickly and easily updates flash devices with new BISO/UEFI Firmware version.

[UEFI BIOS Firmware + Update Utility Tool]()
Coming Soon

The package contains:
* Latest UEFI Firmware binary
  * Firmware name:
  * BIOS version:  1.04
  * Release Date:  
  * SHA1 .zip file:  
* Update Utility Tool
  * EFI shell programming utility
  * Windows 32-bit BIOS programmer
  * Windows 64-bit BIOS programmer
  * Linux 32-bit programmer
  * Linux 64-bit programmer
* Update procedure documentation (.pdf)

Follow the procedure in the .pdf file to update the BIOS/UEFI BIOS firmware using Windows, EFI shell or Linux running on your UDOO BOLT.

<span class="label label-warning">Heads up!</span> Remember that update the BIOS/UEFI firmware will revert the saved configuration to Factory Default.

Please be aware that using **Windows** programmer, it must be run in a Prompt CMD shell with Administrator privileges.

Using **Linux** programmer, *gcc compiler* and *Kernel-headers* are needed and every operation must be done with root/administrator privileges.  
Linux versions used for the test:
* Ubuntu 16.04 - 16.10 - 18.04 - 18.10
* Debian 8.5 - 9
* Fedora 24
* Opensuse 42
