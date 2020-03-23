EAPI (Embedded Application Programming Interface) is a framework
developed by *PICMG®* for *COM Express* modules that gives a common API to unify
software control for:
- System information
- Watchdog timer
- I2C Bus
- Flat Panel brightness control
- User storage area
- GPIO

The EAPI definition is open to be used for other embedded form factors too,
such as SBCs. Read the full specification [here][specs].
Basically you need to include/implement these libraries in you software code to
communicate with the Embedded Controller and use the pinout functionalities.

Download [here][dleapi] the official implementation for UDOO BOLT.

The package contains:
* Latest precompiled EAPI Libraries
* Test application (with sources)
* OS compatibility:
  * Windows 32-bit
  * Windows 64-bit
  * Linux 32-bit
  * Linux 64-bit
* Revision version: 1.8
* Release Date:  2019-11-07
* SHA1 .zip file: 504F790ADBFA1FF690ECB48275C59A5A19F04C55
* Official Documentation inside the package (.pdf)

[specs]: https://www.picmg.org/wp-content/uploads/COM_EAPI_R1_0.pdf
[dleapi]: https://udoo.org/download/files/UDOO_BOLT/tools/EAPI_1_20_20_Build_1657_2019_11_08.zip
