UDOO BOLT is supplied with a [American Megatrends International LLC(AMI)](https://ami.com/en/products/) BIOS/UEFI Firmware.

If you are looking for how to update UEFI Firmware go to the [BIOS-UEFI update](!/Advanced_Topics/BIOS-UEFI_update) section.

It is possible to access to AMI Setup Utility by pressing the escape key (`ESC`) after System power up, during POST phase.

<span class="label label-warning">Heads up!</span> Some wireless or mechanical keyboards that doesn't respect the standard USB HID protocol could doesn't work in the UEFI BIOS Firmware menu. Regarding the wireless keyboards we tested these that are proper working also in the UEFI BIOS menu: [Logitech k400r](http://www.logitech.com/en-us/product/wireless-touch-keyboard-k400r), [Logitech k400 plus](http://www.logitech.com/product/wireless-touch-keyboard-k400-plus), [Microsoft All-in-One Media Keyboard](https://www.microsoft.com/accessories/products/keyboards/all-in-one-media-keyboard/n9z-00013).

<div class="alert alert-danger" role="alert">
  <span class="glyphicon glyphicon-exclamation-sign" aria-hidden="true"></span>
  <span class="sr-only">Warning!</span>
  Warning: Please do NOT "play" with the SCU menu choices if you don't know what you are doing. For example, if you disable USB ports or Video Outputs you will not be able to interact with the SCU to revert this condition. If you stumbling upon this case take a look at the **Restore Factory configuration** section below.
</div>

<span class="label label-warning">Heads up!</span> Since some resolutions or monitors are not managed well by the firmware, if you get a black screen when you try to enter in one of the UEFI Firmware Setup Utility Menu options, try using another Display with a 1920x1080 resolution (HDMI or DisplayPort) or a different cable.  

## UDOO BOLT Hardware and UEFI BIOS User Manual

For a complete explanation of the System Configuration Utility menu items you can download the exhaustive [UDOO BOLT Hardware and UEFI BIOS User Manual](http://download.udoo.org/files/UDOO_BOLT/Doc/UDOO_BOLT_MANUAL.pdf)

## Restore Factory configuration

You can restore the factory default settings pressing the **F9** key.

You can also restore the factory UEFI BIOS configuration with a simple procedure involving the RTC battery: when the board is NOT connected to any power source, **unplug the RTC battery** on the bottom side of the board and keep it unplugged for **at least 1 minute**. Plug the RTC battery again and power up the board, all the configurations should now be reverted to the factory defaults.

<span class="label label-warning">Heads up!</span> Updating the UEFI BIOS to a newer version will also restore the new factory default configuration.
