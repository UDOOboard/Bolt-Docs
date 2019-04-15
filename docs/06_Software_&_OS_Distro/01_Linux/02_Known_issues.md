## amdgpu drivers issue - 'nomodeset' procedure

There is a **known issue** with amdgpu driver which comes with **Ubuntu 18.04 LTS** (and maybe others Linux distros). During and after OS installation it is possible that you may receive a UI after login or you may not.

You can find all the reference about this issue in the amdgpu Documentation (amdgpu_UserGuide) in the driver packages downloadable from the AMD official website.
Check the [Linux Drivers](!Software_&_OS_Distro/Linux/Drivers) section to download the latest driver package.

If you go against this problem during the installation of Ubuntu 18.04 LTS follow the instructions below

To workaround this issue you need to start the installation by adding `nomodeset` parameter to grub.

Adding `nomodeset` doesn’t load amdgpu driver which comes with Ubuntu 18.04 LTS and you will get the UI after login.

Procedure to add `nomodeset` to grub:
* Stop the installation to the grub menu.
* Press `e` to edit the menu entry you choose (e.g *Install Ubuntu*) and it will lead to edit the boot parameters.
* Find the line which ends with `quiet splash` and add `nomodeset` in front of it. So it becomes `nomodeset quiet splash`. Whatever is there in front of it leave it as it is just add `nomodeset` in front of `quiet splash`.
* Press Ctrl+X or F10 to boot with this new parameter.

You can check [this post](https://askubuntu.com/questions/38780/how-do-i-set-nomodeset-after-ive-already-installed-ubuntu/38782#38782) or [this other](https://askubuntu.com/questions/1029624/ubuntu-18-04-live-boot-leads-to-blank-screen) to see an image that will let better understand where to put the `nomodeset` parameter.

Editing the grub like this is just a temporary fix, you probably will need to repeat the procedure after the installation to boot the system.  

After you've installed Ubuntu 18.04 LTS you can install the AMD drivers following the [Linux Drivers](!Software_&_OS_Distro/Linux/Drivers) section, to have a proper working system.

If you don't need the AMD drivers you can set the fix the `nomodeset` boot option permanently so that you don't have to go through this manual procedure again following the instructions in [this post](https://askubuntu.com/a/38782/88802).


## eMMC Installations

Unfortunately, the AMD eMMC Driver is not in the main line Kernel so you will not able to install a Linux distribution.   
For this reason if you try to install a Linux distribution on the eMMC memory of the UDOO BOLT it will not be seen or an error will return.

To install Linux on the eMMC a kernel patch released by AMD is needed.

The package released by AMD guide you through a creation of an Ubuntu 18.04.1 installation image .iso file with the Linux Kernel 4.15 patched .

We already followed the guide and created a custom installable .iso with the AMD eMMC support to allow you to install Ubuntu 18.04.1 LTS on the eMMC of the UDOO BOLT.

You can download the custom image file here: [Ubuntu 18.04.1 UDOO BOLT eMMC installer image](link soon)

Once you have downloaded the image you need to extract it from the .zip file and create a bootable USB drive.  
In the [Getting Started](https://www.udoo.org/get-started-x86/) section you can find a guide of how to install a Linux distro, the example is based on the Ubuntu OS.

<span class="label label-warning">Heads up!</span> We suggest to use [Rufus](https://rufus.ie/) to create the bootable USB drive or a valid Linux alternative. Seems that *Startup Disk Creator* of Ubuntu don't create the bootable USB drive from this image properly.
