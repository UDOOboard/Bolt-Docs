
To start programming the Arduino&reg; Leonardo-compatible embedded microcontroller of the UDOO BOLT you need the `Arduino IDE` or the `Arduino Web IDE`.

You can refer to the [Arduino Leonardo](https://www.arduino.cc/en/Main/Arduino_BoardLeonardo) page and the [Getting Started with the Arduino Leonardo](https://www.arduino.cc/en/Guide/ArduinoLeonardoMicro) page on Arduino&reg;'s website.  

The getting started Arduino page will guide you through the installation of the IDE, Drivers, first example and everything you need to program the Arduino Leonardo and how to use the pinout.  
You can also find useful tutorials and a "please read..." section.

## USB Devices

The USB serial device where you can find the Arduino Leonardo-compatible (ATmega32U4) embedded may vary in accordance with the number of USB devices connected to the board.  
Usually, you should find the Arduino Leonardo-compatible in the `COM3` in **Windows 10** and `/dev/ttyACM0` in **Unix/Linux** OS.

## Linux known issues

### User permissions

Some Linux distributions need to be configured to gain upload permissions to the user to the Arduino tty port.  
If you find some complications in uploading the Arduino sketch(firmware) through the Arduino IDE, try to add your Linux user to the `dialout` group with this command:

    sudo usermod -a -G tty <yourUserName>
    sudo usermod -a -G dialout <yourUserName>

where `<yourUserName>` is your Linux user name. **You will need to log out and log in again for this change to take effect**.

### Sketch upload - ModemManager conflict

If you have issues when trying to upload a sketch on the Arduino Leonardo-compatible ATmega32U4 of UDOO BOLT you probably have a conflict with the program **ModemManager** (installed by default on many Linux distros like Ubuntu).

Modem Manager tries to open any serial port (ttyACM0 of the Arduino Leonardo included) checking if it's a modem and this usually creates conflicts with the upload mechanism.

If you have installed *ModemManager* on your Linux you can try to disable or uninstall it (https://askubuntu.com/questions/216114/how-can-i-remove-modem-manager-from-boot)

Since you probably don't have a modem on your UDOO BOLT you can safely uninstall the package to solve the issue or disable it running the commands:

    sudo systemctl stop ModemManager.service
    sudo systemctl disable ModemManager.service

After this procedure, you should be able to proceed normally and upload the sketch to your board or use the Serial Monitor.
