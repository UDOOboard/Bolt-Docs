UDOO BOLT is supplied with a [American Megatrends International LLC(AMI)](https://ami.com/en/products/) BIOS/UEFI Firmware.

If you are looking for how to update UEFI Firmware go to the [BIOS-UEFI update](!/Advanced_Topics/BIOS-UEFI_update) section.

It is possible to access to AMI Setup Utility by pressing the escape key (`ESC`) after System power up, during POST phase.

<span class="label label-warning">Heads up!</span> Some wireless or mechanical keyboards that doesn't respect the standard USB HID protocol could doesn't work in the UEFI BIOS Firmware menu. Regarding the wireless keyboards we tested these that are proper working also in the UEFI BIOS menu: [Logitech k400r](http://www.logitech.com/en-us/product/wireless-touch-keyboard-k400r), [Logitech k400 plus](http://www.logitech.com/product/wireless-touch-keyboard-k400-plus), [Microsoft All-in-One Media Keyboard](https://www.microsoft.com/accessories/products/keyboards/all-in-one-media-keyboard/n9z-00013).

<div class="alert alert-danger" role="alert">
  <span class="glyphicon glyphicon-exclamation-sign" aria-hidden="true"></span>
  <span class="sr-only">Warning!</span>
  Warning: Please do NOT "play" with the BIOS-UEFI Firmware menu choices if you don't know what you are doing. For example, if you disable USB ports or Video Outputs you will not be able to interact with the BIOS-UEFI Firmware again to revert this condition. If you stumbling upon this case take a look at the **Restore Factory configuration** section below.
</div>

<span class="label label-warning">Heads up!</span> Since some resolutions or monitors are not managed well by the firmware, if you get a black screen when you try to enter in one of the UEFI Firmware Setup Utility Menu options, try using another Display with a 1920x1080 resolution (HDMI or DisplayPort) or a different cable.  

## UDOO BOLT Hardware and UEFI BIOS User Manual

For a complete explanation of the System Configuration Utility menu items you can download the exhaustive [UDOO BOLT Hardware and UEFI BIOS User Manual](http://download.udoo.org/files/UDOO_BOLT/Doc/UDOO_BOLT_MANUAL.pdf)

## Restore Factory configuration

In some cases, a wrong configuration of BIOS parameters could lead the module in an unusable state (i.e. no video output, all USB HID devices disabled).
For these cases, on the module it has been placed a 3-way switch which can be used to restore the BIOS to factory default configuration. To do so, it is necessary to place the contact of the switch in 1-2 position, then turn on the module, wait until the board resets itself then turn off the module. The contact MUST be now placed back to 2-3 position.
During normal use, the contact MUST be always placed in 2-3 position.

<img src="../img/bolt_uefi_restore_switch.png" alt="UDOO versions" class="img-responsive" >

You can restore the factory default settings also from within the BIOS/UEFI settings pressing the **F9** key.

<span class="label label-warning">Heads up!</span> Updating the BIOS/UEFI to a newer version will also restore the new factory default configuration.
