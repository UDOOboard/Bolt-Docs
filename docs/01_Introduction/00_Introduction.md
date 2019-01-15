# UDOO Bolt
**UDOO Bolt** is a portable, breakthrough supercomputer that goes up to *3.6 GHz* thanks to the brand-new **AMD Ryzen&trade; Embedded V1000 SoC**, a top-notch APU, multicore CPU with powerful integrated mobile GPU - *AMD Radeon&trade; Vega 8 or AMD Radeon&trade; Vega 3 Graphics* - and an integrated **Arduino&trade; Leonardo-compatible** platform, all wrapped into one.

On **UDOO Bolt** you can run all the software available for the PC world, from gaming to video streaming, from graphical editors to professional development platforms, plus all the software for the Arduino&trade; Leonardo world, including all the sketches, libraries and the official Arduino&trade; IDE.

UDOO Bolt embeds two processors:
* the new [**AMD Ryzen&trade; Embedded V1000**](https://www.amd.com/en/products/embedded-ryzen-v1000-series), *V1605B* or *1202B*, 14nm, up to a *4-cores/8-threads* CPU, with a thermal design power of just *12-25W*, designed for really fast Ultrathin Notebooks. This processor family brings together the breakthrough performance of the pioneering *AMD “Zen” CPU* and *AMD “Vega” GPU* architectures in a seamlessly-integrated SoC solution that sets a new standard in processing power for next-generation embedded designs.
* the [**Atmel&reg; ATmega32U4**](https://www.microchip.com/wwwproducts/en/ATmega32u4) 8-bit AVR microcontroller, the same of *Arduino&trade; Leonardo*.

While the AMD Ryzen&trade; Embedded V1000 processor can run all the Windows 10 and Linux 64bit Distros you want to use as desktop PC, the Atmel&reg; ATmega32U4 allows easy access to a Arduino&trade; Leonardo environment.

Download the [**User Manual**](http://download.udoo.org/files/UDOO_BOLT/Doc/UDOO_BOLT_MANUAL.pdf) to have more complete explanation of the UDOO BOLT hardware and features.

<hr/>

<span class="label label-warning">Heads up!</span> In order to prevent damages to your board, remember to:

* CE certification retained using only the UDOO BOLT qualified Power Supply. When not using UDOO Bolt qualified Power Supply, use 19VDC (min 60W power) PSUs certified for your country(make sure that the power cable is less than 3 mt. long).
* This product should be operated in a well-ventilated environment and, if used inside a case, the case should not be covered.
* This product should be elevated on a stable, flat, electrically non-conductive surface whilst in operation, and clear from any object that can induce a short-circuit.
* Do not expose it to water, moisture or heat from any source; UDOO BOLT is designed for reliable operation at normal ambient room temperatures.
* Avoid handling the warm and moving parts (like the fan) and generally the printed circuit board while it is powered.
* Only handle by the edges to minimise the risk of electrostatic discharge damage.
* Take care whilst handling to avoid mechanical or electrical damage to the printed circuit board and connectors. Also use a grounded wrist strap or touch a safely grounded object before you handle components.
* Never provide more than 5V in input to the GPIOs of the Arduino Leonardo(Atmel&reg; ATmega32U4), and never provide more than 3.3V in input to the GPIOs of the Embedded Controller.
* Do not use a *NON*-standard USB 3.0 peripheral. If you use a non-standard USB 3.0 peripheral with an external power plug, this could send back the power source to the UDOO Bolt board with the risk of damage.
* The most important safety rule of all: **Always Be Careful! (ABC)**


## Lineup
UDOO Bolt retail line up consists of two models.

<img src="../img/x86_lineup.png" alt="UDOO versions" class="img-responsive" >


## Technical specifications

<img src="../img/x86_ultra_top_rotate.png" alt="UDOO Boards" class="img-responsive pull-right" height="441px" width="350px"  style="margin-bottom:20px; margin-left:30px;">

* Processor:
  * CPU AMD Ryzen&trade; Embedded V1605B SoC up to 3.6 GHz (V8 version)
  * CPU AMD Ryzen&trade; Embedded V1202B SoC up to 3.2 GHz (V3 version)
* GPU:
  * AMD Radeon™ Vega 8 Graphics - 8 GPU Compute Units (V8 version)
  * AMD Radeon™ Vega 3 Graphics - 3 GPU Compute Units (V3 version)
* RAM:
  * 2x Slot SO-DIMM Dual-channel 64-bit DDR4 2400 MT/s with ECC support up to 32GB
* Atmel&reg; ATmega32U4 8-bit AVR RISC-based microcontroller.
* Video interfaces:
  * 2x HDMI 1.4/2.0a (CEC)
  * 2x USB Type-C (DP alternate mode)
* Storage:
  * 1x 32GB eMMC 5.0 High Speed Drive
  * 1x SSD SATA module's Slot M.2 Socket 2 Key B 2242/2260 (featured also PCI-e x2)
  * 1x NVMe modules Slot M.2 Socket 3 Key M 2280 (PCI-e x4 Gen 3 interface)
  * 1x SATA III 6Gbit/s standard connector
* Networking:
  * 1x Gigabit Ethernet LAN interface
  * 1x M.2 Key E slot for optional Wireless(WiFi+BT) combo module
* Audio interfaces:
  * HD Audio Codec Realtek ALC888S
  * Microphone + Headphone Combo Connector (TRRS)
  * Pre-amplified stereo Speaker Connectors (up to 3W)
  * Digital Optical audio S/PDIF and analog stereo output combo jack 3.5mm connector
* 2x USB 3.0 type-A sockets
* 2x USB Type-C :
  * USB 3.1 Gen 2
  * DisplayPort Alternate Mode
  * Dual Role Port (DRP) USB Power Delivery (USB-PD) 3.0
* Embedded Controller I/O :
  * 2x UART ports*
  * 2x I2C interface*
  * 1x SPI interface*
  * 1x Keyboard Scan interface*
  * 1x FAN Controller*
  * up to 10x GPIO
* Power In:
  * 19V DC Power Jack at least 3A.
  * USB Type-C power in. PD sink profile 20V/3A(60W).
* RTC Battery Connector + RTC Coin Battery
* Bi-color Power Status LED
* Arduino&trade; Leonardo-Compatible I/O :
  * 12x analog inputs*
  * up to 23x digital input/output (7 PWM)*
  * 1x UART 1x I2C 1x SPI*
  * 3x Grove connectors:
     * 1x ANALOG INPUT, 1x UART or DIGITAL I/O, 1x I2C or DIGITAL I/O
* Dimensions: 12cm x 12cm  -  4.72” x 4.72”

&#42;Available on Pin Headers

Visit the official accessories sections.

## Community
* Official web site [www.udoo.org](https://www.udoo.org)
* Official web site dedicated page: tbu
* Official forum [www.udoo.org/forum](https://www.udoo.org/forum/index.php)

### Forums
The official UDOO forums can be found at [www.udoo.org/forum](https://www.udoo.org/forum)

The forum search facility has been tweaked to allow more general searching.
**Please** do a search before making a post as the issue may already have been raised and answered.

### IRC channel
There is an (unofficial) UDOO discussion channel on IRC. Using the IRC client of your choice, use server information: `irc.freenode.net`. Room name is `#udoo`.


### Social networks
 * [Facebook fan page](http://www.facebook.com/udooboard)
 * [Twitter](http://twitter.com/UDOO_Board)
 * [Google+](https://plus.google.com/u/0/110742692974455430878/posts)
 * [YouTube](http://www.youtube.com/channel/UCXv5UyGn5jArK8xOAmuSeHg)
 * [Instagram](https://www.instagram.com/udoo_board/)


<!-- Google Code -->
<script type="text/javascript">
var google_conversion_id = 983836026;
var google_custom_params = window.google_tag_params;
var google_remarketing_only = true;
</script>
</noscript>
