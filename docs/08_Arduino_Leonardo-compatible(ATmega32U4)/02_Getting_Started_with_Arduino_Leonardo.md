
To start programming the Arduino&reg; Leonardo-compatible embedded microcontroller of the UDOO BOLT you need the `Arduino IDE` or the `Arduino Web IDE`.

You can refer to the [Arduino Leonardo](https://www.arduino.cc/en/Main/Arduino_BoardLeonardo) page and the [Getting Started with the Arduino Leonardo](https://www.arduino.cc/en/Guide/ArduinoLeonardoMicro) page on Arduino&reg;'s website.  

The getting started Arduino page will guide you through the installation of the IDE, Drivers, first example and everything you need to program the Arduino Leonardo and how to use the pinout.  
You can also find useful tutorials and a useful *"please read..."* section with lot of specific information for Arduino Leonardo.

# USB Devices

The USB serial device where you can find the Arduino Leonardo-compatible (ATmega32U4) embedded may vary in accordance with the number of USB devices connected to the board.  
Usually, you should find the Arduino Leonardo-compatible in the `COM3` in **Windows 10** and `/dev/ttyACM0` in **Unix/Linux** OS.

# Linux Installation

There are **known issues** with the **Arduino&reg; IDE** on **Linux** that can lead to malfunctions and difficulties in uploading sketches.  
These known issues have been solved by Arduino (from version *1.8.6* of the IDE) with a script to launch immediately after installing the IDE on the system. We suggest so to use the scripts contained in the Arduino package to install the software and fix these issues.  
After downloading the package from the official website, and extracting it, you should then run the following commands in a terminal to install the Arduino IDE on your Linux system:

    sudo ./install.sh
    ./arduino-linux-setup.sh $USER



## Known issues

<span class="label label-warning">Heads up!</span> The `arduino-linux-setup.sh` above will solve the issues of *user permissions* and *sketch upload* described below. If you are working with an old version of the IDE where this script is not present you can try to copy it from a new version or manually fix the issues as described below.

### User permissions

Some Linux distributions need to be configured to gain upload permissions to the user to the Arduino tty port.  
If you find some complications in uploading the Arduino sketch(firmware) through the Arduino IDE, try to add your Linux user to the `dialout` group with this command:

    sudo usermod -a -G tty <yourUserName>
    sudo usermod -a -G dialout <yourUserName>

where `<yourUserName>` is your Linux user name. **You will need to log out and log in again for this change to take effect**.

### Sketch upload

#### ModemManager conflict

If you have issues when trying to upload a sketch on the Arduino Leonardo-compatible ATmega32U4 of UDOO BOLT you probably have a conflict with the program **ModemManager** (installed by default on many Linux distros like Ubuntu).

Modem Manager tries to open any serial port (ttyACM0 of the Arduino Leonardo included) checking if it's a modem and this usually creates conflicts with the upload mechanism.

If you have installed *ModemManager* on your Linux you can try to disable or uninstall it (https://askubuntu.com/questions/216114/how-can-i-remove-modem-manager-from-boot)

Since you probably don't have a modem on your UDOO BOLT you can safely uninstall the package to solve the issue or disable it running the commands:

    sudo systemctl stop ModemManager.service
    sudo systemctl disable ModemManager.service

After this procedure, you should be able to proceed normally and upload the sketch to your board or use the Serial Monitor.

The solution of this issue was found in [this thread](https://forum.arduino.cc/index.php?topic=129647.msg2378141#msg2378141) of the Arduino Forum.

#### How to restore the correct uploading state of sketches

If you have not taken into account the possible conflict between ModemManager and sketch upload and you have not followed the instructions listed above, it may happen that the Arduino microcontroller is set in a state where the operating system *does not see the serial port*. This no longer allows you to load the sketch also using a different operating system.

To exit from this state you can try to perform the procedure indicated by the [Arduino Leonardo page](https://www.arduino.cc/en/Guide/ArduinoLeonardoMicro#toc12).  
Pressing the Arduino physical reset button with the right timing it is possible to load a sketch when the serial port of the bootloader is exposed and restore the correct functioning of the ATmega32U4 microcontroller of Arduino Leonardo.

Summarising, you need to hit the Arduino IDE *Upload* button and press the Arduino physical *reset* button with the right timing immediately after you see the message "*Uploading...*" appear in the software's status bar.  
Enable the verbose option of the Arduino IDE upload process can be very useful to understand when to correctly press the reset button . To do so, go to the menu `File -> Preference` and check the `upload` option box in the "*Show verbose output during*" section.  
The correct time to press the reset button is when starts to appear `PORT {} / {} => {}` in the log. The IDE will see that port appear and perform the upload using it.

<span class="label label-warning">Heads up!</span> This won't work if something interferes with the board's USB communication so please, be sure to have resolved such issues as the conflict with ModemManager above.
