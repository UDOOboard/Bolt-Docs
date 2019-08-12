If you find any problem in the proper working of UDOO BOLT you can consult this section.

## My UDOO BOLT doesn't boot or restart itself continuously

If it seems that your UDOO BOLT does NOT boot or that it restarts all the time, please check these points:

- When the power jack is inserted the board does not start automatically. The power status LED is yellow/amber/orange and the board is in the power off state. To turn on UDOO BOLT you have to press the small **power button** on the front of the board. The status LED turns green when the board is powered on. Check the power button position in the [Hardware Reference - Overview](!/Hardware_References/Overview) page.

- Check the **power source** you are applying to UDOO BOLT. Please, follow the [Power Sources](!/Hardware_References/Power_Sources) page or consult the [User Manual](http://download.udoo.org/files/UDOO_BOLT/Doc/UDOO_BOLT_MANUAL.pdf) to learn more about the power supply needed by the board for normal operation.

- Check that the restore factory configuration **switch** is in the right position for normal operation, otherwise the board will restart continuously. You can find info about that switch in the [BIOS-UEFI Firmware](!/Advanced_Topics/BIOS-UEFI_firmware) page or consulting the [User Manual](http://download.udoo.org/files/UDOO_BOLT/Doc/UDOO_BOLT_MANUAL.pdf).

## I can't install a Linux distro on UDOO BOLT's eMMC

If you try to **install** a **Linux** distribution on the **eMMC** of the UDOO BOLT but the eMMC memory is not seen by the installer wizard see the _eMMC Installations_ section in the [Linux - Known issues](!/Operating_Systems/Linux/Known_issues) page.

## I have trouble uploading the Arduino Leonardo sketch running Linux

If you have any trouble **uploading** the **Arduino sketch** running **Linux**, check the _Linux known issues_ section in the [Getting Started with Arduino Leonardo](!/Arduino_Leonardo-compatible(ATmega32U4)/Getting_Started_with_Arduino_Leonardo) page.
