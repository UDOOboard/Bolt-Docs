## amdgpu drivers issue - 'nomodeset' procedure

There is a **known issue** with amdgpu driver which comes with **Ubuntu 18.04 LTS** (and maybe others Linux distros). During and after OS installation it is possible that you may receive a UI after login or you may not.

<span class="label label-warning">Heads up!</span> Ubuntu 18.10 "Cosmic Cuttlefish" and Ubuntu 19.04 "Disco Dingo" are not affected by this issue so you don't need to use this procedure.

You can find all the references about this issue in the amdgpu Documentation (amdgpu_UserGuide) in the driver packages downloadable from the AMD official website.
Check the [Linux Drivers](!Operating_Systems/Linux/Drivers) section to download the latest driver package.

If you experience this problem during the installation of Ubuntu 18.04 LTS follow the instructions below

To workaround this issue you need to start the installation by adding `nomodeset` parameter to grub.

Adding `nomodeset` doesn’t load amdgpu driver which comes with Ubuntu 18.04 LTS and you will get the UI after login.

Procedure to add `nomodeset` to grub:
* Stop the installation to the grub menu.
* Press `e` to edit the menu entry you choose (e.g *Install Ubuntu*) and it will lead to edit the boot parameters.
* Find the line which ends with `quiet splash` and add `nomodeset` in front of it. So it becomes `nomodeset quiet splash`. Whatever is there in front of it leave it as it is just add `nomodeset` in front of `quiet splash`.
* Press Ctrl+X or F10 to boot with this new parameter.

You can check [this post](https://askubuntu.com/questions/38780/how-do-i-set-nomodeset-after-ive-already-installed-ubuntu/38782#38782) or [this other post](https://askubuntu.com/questions/1029624/ubuntu-18-04-live-boot-leads-to-blank-screen) to see an image that will let better understand where to put the `nomodeset` parameter.

Editing the grub like this is just a temporary fix, you probably will need to repeat the procedure after the installation to boot the system.  

After you've installed Ubuntu 18.04 LTS you can install the AMD drivers following the [Linux Drivers](!Operating_Systems/Linux/Drivers) section, to have a proper working system.

If you don't need the AMD drivers you can set the fix the `nomodeset` boot option permanently so that you don't have to go through this manual procedure again following the instructions in [this post](https://askubuntu.com/a/38782/88802).


## eMMC Installations

<span class="label label-info">Info!</span> The **Linux Kernel** mainline with version **>=5.2.5** includes support for the **AMD eMMC driver** for **Ryzen v1000 embedded** series processors. Some Linux distributions with a kernel version >=5.2.5 such as *ArchLinux* or *Mangiaro* have already been released and support correctly the UDOO BOLT eMMC.

Unfortunately, the AMD eMMC driver for the Ryzen v1000 embedded series processors was not included in the mainline **Linux Kernel** before version **5.2.5**, so it will not be possible to install a standard Linux distribution on the eMMC with an older kernel than that version(< 5.2.5) onboard the UDOO BOLT eMMC without some tweaks.

To install a Linux distro with a kernel older than 5.2.5 on the eMMC, a kernel patch released by AMD is needed.  
The package released by AMD is going to guide you through a creation of a *Ubuntu 18.04.1* installation image .iso file with the Linux Kernel *4.15.18* patched to support the AMD eMMC driver(you can find the patch package at the end of this section).

We already followed the guide and created a custom installable .iso with the AMD eMMC support to allow you to install **Ubuntu 18.04.1 LTS** on the **eMMC** of the UDOO BOLT.
You can download the custom image file here:  
[**Ubuntu 18.04.1 - UDOO BOLT eMMC installer image**](http://download.udoo.org/files/UDOO_BOLT/Ubuntu/ubuntu-18.04.1.bolt_emmc.zip)  
SHA1SUM: *6aa0c46436945074b571aae37a5923fcb4c02def  ubuntu-18.04.1.bolt_emmc.zip*

Once you have downloaded the image you need to extract it from the .zip file and create a bootable USB drive.  
In the [Getting Started](https://www.udoo.org/get-started-bolt/) section you can find a guide on how to install a Linux distro, the example is based on the Ubuntu OS.

<span class="label label-warning">Heads up!</span> We suggest to use [Rufus](https://rufus.ie/) to create the bootable USB drive or a valid Linux alternative. Seems that *Startup Disk Creator* of Ubuntu doesn't create the bootable USB drive from this image properly.

<span class="label label-warning">Heads up!</span> Unfortunately, the image created following the AMD guide to apply the eMMC patch does not take into account the previous problem with AMD amdgpu graphics drivers, so you also need to follow the previous section with the `nomodeset` procedure to install the OS and use it.

If you want to fix the amdgpu driver issue installing the [AMD kernel and drivers](!Operating_Systems/Linux/Drivers) you have to take into account that the binaries released by AMD do not integrate the eMMC support patch into the kernel, so once installed you'll find again the eMMC error in the boot that does not allow you to use the OS.

We then recompiled the AMD kernel source contained in the driver package by adding the patch for eMMC support and you can download them here:  
[udoo_bolt_linux-4.19.8_amd64_amdgpu_emmc.tar.gz](http://download.udoo.org/files/UDOO_BOLT/tools/udoo_bolt_linux-4.19.8_amd64_amdgpu_emmc.tar.gz)  
SHA1SUM: *bd546f5497069ce35af5c18112ebd0f314fa6115 udoo_bolt_linux-4.19.8_amd64_amdgpu_emmc.tar.gz*

Extract the package and install the custom kernel using the command `dpkg -i` with the three .deb files in the package.

Summing up, the right procedure to have a proper working OS with eMMC support and amdgpu support is this one:
* Download the *Ubuntu 18.04.1 UDOO BOLT eMMC installer image* and create a USB installation bootable drive with Rufus or similar.
* Install *Ubuntu 18.04.1* using the `nomodeset` parameter at grub.
* Reboot the OS (you'll probably need again to use the `nomodeset` parameter) and install the [AMD kernel and drivers 4.19.8](!Operating_Systems/Linux/Drivers) with the official AMD package using the binaries.
* Install the custom *kernel 4.19.8* you can find above.
* Reboot the system with the new kernel.

If you want to create a distro integrating by your own the AMD eMMC patch for the Ryzen v1000 processors series in the Linux Kernel you can download this package released by AMD:  
[emmc_v1000_patch.zip](http://download.udoo.org/files/UDOO_BOLT/tools/emmc_v1000_patch.zip)  
SHA1SUM: *6FB569D462701E16F70405BC107CE0F91C87F26C  emmc_v1000_patch.zip*
