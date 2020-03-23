UDOO BOLT is supplied with [American Megatrends International LLC(AMI)](https://ami.com/en/products/)'s BIOS/UEFI Firmware.

It is possible to access the AMI Setup Utility by pressing the escape key (`ESC`) after System power up, during POST phase.

<span class="label label-warning">Heads up!</span> Some wireless or mechanical keyboards that doesn't respect the standard USB HID protocol could doesn't work in the UEFI BIOS Firmware menu. Regarding the wireless keyboards we tested these that are proper working also in the UEFI BIOS menu: [Logitech k400r](http://www.logitech.com/en-us/product/wireless-touch-keyboard-k400r), [Logitech k400 plus](http://www.logitech.com/product/wireless-touch-keyboard-k400-plus), [Microsoft All-in-One Media Keyboard](https://www.microsoft.com/accessories/products/keyboards/all-in-one-media-keyboard/n9z-00013).

<p style="background-color: rgba(255, 170, 50, 0.3);padding: 20px;border-left: 5px solid orange; border-radius: 4px; color:rgb(45, 45, 45);">
Please do NOT "play" with the BIOS-UEFI Firmware menu choices if you don't know what you are doing. For example, if you disable USB ports or Video Outputs you will not be able to interact with the BIOS-UEFI Firmware again to revert this condition. If you stumbling upon this case take a look at the <i>Restore Factory configuration</i> section below.
</p>

<span class="label label-warning">Heads up!</span> Since some resolutions or monitors are not managed well by the firmware, if you get a black screen when you try to enter in one of the UEFI Firmware Setup Utility Menu options, try using another Display with a 1920x1080 resolution (HDMI or DisplayPort) or a different cable.  

### UDOO BOLT Hardware and UEFI BIOS User Manual

For a complete explanation of the System Configuration Utility menu items you can download the exhaustive [UDOO BOLT Hardware and UEFI BIOS User Manual](https://udoo.org/download/files/UDOO_BOLT/Doc/UDOO_BOLT_MANUAL.pdf)

### Restore Factory configuration

In some cases, a wrong configuration of BIOS parameters could lead the module in an unusable state (i.e. no video output, all USB HID devices disabled).
For these cases, on the module it has been placed a 3-way switch which can be used to restore the BIOS to factory default configuration. To do so, it is necessary to place the contact of the switch in 1-2 position, then turn on the module, wait until the board resets itself then turn off the module. The contact MUST be now placed back to 2-3 position.
During normal use, the contact MUST be always placed in 2-3 position.

<img src="../img/bolt_uefi_restore_switch.png" alt="UDOO versions" class="img-responsive" >

You can restore the factory default settings also from within the BIOS/UEFI settings pressing the **F9** key.

<span class="label label-warning">Heads up!</span> Updating the BIOS/UEFI to a newer version will also restore the new factory default configuration.

## BIOS/UEFI Update

At the following link you can find the latest BIOS/UEFI Firmware and the BIOS/UEFI Update Utility to quickly and easily update the UDOO BOLT with the new BIOS/UEFI Firmware version.

<span class="label label-warning">Heads up!</span> Please read carefully all the following information in this page and in the documentation file inside the package before to flash the new BIOS/UEFI

Please be aware that using **Windows** programmer, it must be run in a Prompt CMD shell with Administrator privileges.

Using **Linux** programmer, *gcc compiler* and *Kernel-headers* are needed and every operation must be done with root/administrator privileges.  

<ul style="background-color: rgba(255, 170, 50, 0.3);padding: 20px;border-left: 5px solid orange; border-radius: 4px; color:rgb(45, 45, 45);">
  <li>DO NOT POWER OFF the board while flashing. DO NOT interrupt the process while is running.</li>
  <li>Please use <strong>19V Power Supply</strong>, not the USB-C power.</li>
  <li>After flashing is complete, power off the board, <strong>disconnect and reconnect the power cable</strong>.</li>
  <li>When you reconnect the power, wait <strong>up to 3 minutes and a couple of reboots</strong> until you see the newer version of the firmware of Embedded Controller and USB-C Controller in the configuration screen.</li>
  <li>It takes a few restarts for the update to be completely installed, and there's no visual feedback on that yet. In the meantime, the system and the boot phase might be slower.</li>
</ul>

Download here the [UEFI BIOS Firmware + Update Utility Tool]() package.

The package contains:
* Latest UEFI Firmware binary
  * BIOS version:  1.07
  * Release Date:  19/03/2020
  * SHA1 .zip file:  
* Update Utility Tool
  * EFI shell programming utility
  * Windows 32-bit BIOS programmer
  * Windows 64-bit BIOS programmer
  * Linux 32-bit programmer
  * Linux 64-bit programmer
* Update procedure documentation (.pdf)

Follow the procedure in the `APN - BIOS programming using AFU.pdf` file to update the BIOS/UEFI BIOS firmware using Windows, EFI shell or Linux running on your UDOO BOLT.

<span class="label label-info">Note</span> Remember that updating the BIOS/UEFI firmware will revert the saved configuration to Factory Default.
