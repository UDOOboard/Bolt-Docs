If you find any problem in the proper working of UDOO BOLT, please consult this section.

## My UDOO BOLT doesn't boot or restart itself continuously

If your UDOO BOLT does NOT boot or restarts all the time, please check the following points:

- When the power jack is inserted the board does not start automatically. The power status LED is *yellow/amber/orange* and the board is in the power off state. To turn on UDOO BOLT you have to press the small **power button** on the front of the board. The status LED turns green when the board is powered on. Check the power button position in the [Hardware Reference - Overview](!/Hardware_References/Overview) page.

- Check the **power source** you are applying to UDOO BOLT. Please, follow the [Power Sources](!/Hardware_References/Power_Sources) page or consult the [User Manual](http://download.udoo.org/files/UDOO_BOLT/Doc/UDOO_BOLT_MANUAL.pdf) to learn more about the power supply needed by the board for normal operation.

- Check that the restore factory configuration **switch** is in the right position for normal operation, otherwise the board will restart continuously. You can find info about that switch in the [BIOS-UEFI Firmware](!/Advanced_Topics/BIOS-UEFI_firmware) page or consulting the [User Manual](http://download.udoo.org/files/UDOO_BOLT/Doc/UDOO_BOLT_MANUAL.pdf).

## I can't install Linux distros on eMMC

If you are trying to **install** a **Linux** distribution on the UDOO BOLT **eMMC** but it is not seen by the installer wizard, please follow the *eMMC Usage and Installations* section in the [Linux - Known issues](!/Operating_Systems/Linux/Known_issues#page_eMMC-Usage-and-Installation) page. Probably the Linux distro you are trying to install use a Linux Kernel older than the 5.2.5 version.  
A Ubuntu 19.04 optimized version for UDOO BOLT that solves this issue is downloadable from the [Linux section](!/Operating_Systems/Linux/index#page_Ubuntu-19-04-Disco-Dingo-with-amdgpu-graphics-and-eMMC-support).

## I can't upload sketches to Arduino Leonardo

If you have any trouble uploading **Arduino sketches** running **Linux**, check the *Linux - known issues* section in the [Getting Started with Arduino Leonardo](!/Arduino_Leonardo-compatible(ATmega32U4)/Getting_Started_with_Arduino_Leonardo#page_Known-issues) page.  
Here you can find a procedure for trying to [restore the correct uploading state of sketches](!/Arduino_Leonardo-compatible(ATmega32U4)/Getting_Started_with_Arduino_Leonardo#page_How-to-restore-the-correct-uploading-state-of-sketches).
