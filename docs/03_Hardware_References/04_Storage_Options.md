### eMMC onboard

UDOO BOLT features an embedded multi media card memory of 32GB.  

The eMMC use a **e.MMC 5.1 HS400** compliant interface.

<span class="label label-warning">Heads up!</span> As a flash-based storage device, excessive drive access, particularly write commands, reduces its useful life. Therefore, it is strongly suggested to NOT create a swap partition on the eMMC device.

### M.2 SATA/PCI-e x2 Slot: Socket 2 Key B type 2242/3042/2260

The mass storage capabilities of the UDOO BOLT are completed by an M.2 SSD Slot, which allow plugging **M.2 Socket 2 Key B** Solid State Drives with *SATA* interface or *PCI-e x2* interface (*PCI-e x1* is also supported).  

The connector used for the M.2 SATA/PCI-e slot is *CN18*, which is a standard 75 pin M.2 Key B connector, located at the bottom of the board.

On the UDOO BOLT board there is also a Threaded Spacer which allows the placement of M.2 Socket 2 Key B SATA/PCI-e modules in `2260` size.

It is possible to place also modules in `2242` and `3042` size, by using a M/F Spacer which allows fixing the M.2 module on the spacer already available on the PCB, deemed for the fixing of the M.2 Wireless module.

In the [Official Accessories](!Hardware_&_Accessories/Official_Accessories) section you can find a *M.2 SSD Transcend MTS600 2260* drive compatible with this connector, available in the UDOO shop.

### M.2 NVMe Slot: Socket 3 Key M Type 2280

Another possibility for connecting mass storage devices is given by the **M.2 Key M** Slot, which allows the plugging of M.2 High Capacity SSD NVMe drives with PCI-e x4 interface.

The connector used for the M.2 SSD slot is *CN17*, which is a standard 75 pin M.2 Key M connector, located at the bottom of the board.

On the UDOO BOLT board there is also a Threaded Spacer which allows the placement of M.2 Socket 3 Key M PCI-e SSD modules in `2280` size.

### SATA

The AMD Ryzen™ Embedded V1000 family of Processors embed a SATA Controller, which offers two **SATA III 6.0 Gbps** interfaces.

Of these interfaces, one SATA channel is carried out to a standard male S-ATA connector, *CN14* (the other SATA channel is available on the M.2 Key B socket).

A dedicated power connector *CN15*, can be used to give supply to *2.5"* Hard Disk Drives (or Solid State Drives) connected to the SATA male connector.  
The dedicated power connector is a 4-pin male connector. You can find this cable in the [SATA data and power cables](http://shop.udoo.org/sata-data-and-power-cables-for-udoo-x86.html) kit.

<span class="label label-warning">Heads up!</span> To connect a *3.5"* Hard Drive you need to provide SATA +5V+12V combo power supply from an external source.
