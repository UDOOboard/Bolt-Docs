
To start programming the Arduino&reg; Leonardo-compatible embedded microcontroller of the UDOO BOLT you need the `Arduino IDE` or the `Arduino Web IDE`.

You can refer the [Arduino Leonardo](https://www.arduino.cc/en/Main/Arduino_BoardLeonardo) page and the [Getting Started with the Arduino Leonardo](https://www.arduino.cc/en/Guide/ArduinoLeonardoMicro) page of the Arduino&reg; website.  

The getting started Arduino page will guide you through the installation of the IDE, Drivers, first example and other than everything you need to program the Arduino Leonardo and use the pinout.  
You can also find useful tutorials and a "please read..." section.

## USB Devices

The USB serial device where you can find the Arduino Leonardo-compatible (ATmega32U4) embedded may vary in accordance with the number of USB devices connected to the board.  
Usually, you should find the Arduino Leonardo-compatible in the `COM3` in **Windows 10** and `/dev/ttyACM0` in **Unix/Linux** OS.

## Linux known issues

Some Linux distributions need to be configured to gain upload permissions to the user.  
If you found some difficult to upload the Arduino sketch(firmware) throgh the Arduino IDE try to add the Linux user to the `dialout` group with this command:

    sudo adduser $USER dialout
