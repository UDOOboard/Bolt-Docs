<p style="background-color: rgba(255, 170, 50, 0.3);padding: 20px;border-left: 5px solid orange; border-radius: 4px; color:rgb(45, 45, 45);">
The reported known issues in this page are already solved in the Ubuntu 19.04 image we've published in the start page of the <a href="./index.html">Linux section</a>.
</p>

## amdgpu drivers issue in Ubuntu 18.04 - 'nomodeset' procedure

<span class="label label-info">Info!</span> Newer versions of Ubuntu than 18.04 are not affected by this issue so you don't need to use this procedure.

There is a *known issue* with **amdgpu driver** which comes with **Ubuntu 18.04 LTS** (and maybe others Linux distros). During and after OS installation it is possible that you may receive a UI after login or you may not.

You can find all the references about this issue in the amdgpu Documentation (amdgpu_UserGuide) in the driver packages downloadable from the AMD official website.
Check the [**Linux Drivers**](!Operating_Systems/Linux/Drivers) section to download the latest driver package.

If you experience this problem during the installation of Ubuntu 18.04 LTS (or in a different Linux distro) follow the instructions below or install a newer version of Ubuntu or the optimized version of Ubuntu 19.04 we've published in the start page of the [Linux section](!/Operating_Systems/Linux/index)

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

## eMMC Usage and Installation

<span class="label label-info">Info!</span> The **Linux Kernel** mainline with version **>=5.2.5** includes support for the **AMD eMMC driver** for **Ryzen v1000 embedded** series processors. Some Linux distributions with a kernel version >=5.2.5 such as *ArchLinux* or *Manjaro* have already been released and support correctly the UDOO BOLT eMMC.

Unfortunately, the AMD eMMC driver for the Ryzen v1000 embedded series processors was not included in the mainline **Linux Kernel** before version **5.2.5**, so it will not be possible to install a standard Linux distribution on the eMMC with an older kernel than that version(< 5.2.5) onboard the UDOO BOLT eMMC without some tweaks.

To install a Linux distro with a kernel older than 5.2.5 on the eMMC, a kernel patch released by AMD is needed.  
The package released by AMD is going to guide you through a creation of a *Ubuntu 18.04.1* installation image .iso file with the Linux Kernel *4.15.18* patched to support the AMD eMMC driver, you can download the patch here:
[emmc_v1000_patch.zip](https://udoo.org/download/files/UDOO_BOLT/tools/emmc_v1000_patch.zip)  
SHA1SUM: *6FB569D462701E16F70405BC107CE0F91C87F26C  emmc_v1000_patch.zip*

We recompiled the AMD kernel source contained in the GPU driver package by adding the patch for eMMC support and you can download them here:  
[udoo_bolt_linux-4.19.8_amd64_amdgpu_emmc.tar.gz](https://udoo.org/download/files/UDOO_BOLT/tools/udoo_bolt_linux-4.19.8_amd64_amdgpu_emmc.tar.gz)  
SHA1SUM: *bd546f5497069ce35af5c18112ebd0f314fa6115 udoo_bolt_linux-4.19.8_amd64_amdgpu_emmc.tar.gz*

Extract the package and install the custom kernel using the command `dpkg -i` with the three .deb files in the package.
