### Overview

On this page you will find some information and tips about the fan above the heatsink of the processor.

The fan that cools the processor is a 5V powered fan with PWM signal speed management and is managed entirely by the board's Embedded Controller.

The full management of the fan settings described below is possible starting from BIOS/UEFI Firmware version 1.07.  
<span class="label label-warning">Heads up!</span>  Please, always keep updated the BIOS/UEFI Firmware of your UDOO BOLT to have the latest features and bugfix available.  


### BIOS/UEFI Fan Settings

Here a detailed description of the fan settings and its default values.


      Advanced
      --> Embedded Controller
          --> Internal Fan settings

              Enhanced 3 wire RPM measurement        <Disabled>
              Automatic Temperature FAN Control      <Enabled>
                AC0 Temperature (C)                  <75>
                AC1 Temperature (C)                  <45>
                Temperature Hysteresis               6
                FAN Duty Cycle (%) Above AC1         60
                Speed change duration                0



**Enhanced 3 wire RPM measurement** refers to an algorithm necessary for the consistent reading of the current fan speed to respond to the tachometer signal. This data is made available by EAPI libraries.
By default it is disabled.

**AC0 Temperature** indicates the temperature above which the fan start turns on at full 100% speed.

**AC1 Temperature** indicates the temperature above which the fan start turns on at the % speed indicated by the *FAN Duty Cycle (%) Above AC1* value.

**Temperature Hysteresis** is the threshold of hysteresis after which the fan will restart once it has shut down after dissipating heat.

**FAN Duty Cycle (%) Above AC1** is the percentage speed at which the fan turns when the processor is in the temperature range between AC1 and AC0.

**Speed change duration** indicates the time with which the speed changes linearly from one value to another (it is a ramp in practice, if set to 0 the fan will start directly at the right speed, if other values are set the fan will start more slowly and arrive at the selected speed more gradually).


<p style="background-color: rgba(255, 170, 50, 0.3);padding: 20px;border-left: 5px solid orange; border-radius: 4px; color:rgb(45, 45, 45);">
If the fan is changed and a fan that does <strong>not handle PWM</strong> is used, it is important to set the values for <strong>FAN Duty Cycle values</strong> to <strong>100</strong> and <strong>Speed change duration</strong> to <strong>0</strong>.
</p>

<p style="background-color: rgba(255, 170, 50, 0.3);padding: 20px;border-left: 5px solid orange; border-radius: 4px; color:rgb(45, 45, 45);">
If you are one of the <strong>Kickstarter</strong> users and you see a <strong>green dot</strong> on one side of the fan, your fan is not handling the PWM speed correctly, so please set the <strong>FAN Duty Cycle values</strong> to <strong>100</strong> and <strong>Speed change duration</strong> to <strong>0</strong>.
</p>
