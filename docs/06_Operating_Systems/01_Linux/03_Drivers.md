AMD Vega graphics card used by the UDOO BOLT is fully supported in Linux.

In this page you can find anything you need to know regarding the Linux Drivers.

## AMDGPU and AMDGPU-Pro

**AMDGPU** is AMD's fully *open source* unified graphics Linux driver included in the mainline Linux Kernel for Vega GPUs and Raven Ridge APUs.

**AMDGPU-PRO** is the *closed source* component that operates on top of the open source AMDGPU for alternative 3D application.

from the *Gentoo Linux* docs we report an exhaustive explanation of the situations in which it is convenient to use one or other version of the driver:
> Users whose main use for their graphics card is gaming and other general home-use graphical hardware acceleration should use the open source AMDGPU drivers, since the performance of the open source drivers can be as much 100% more compared to AMDGPU-Pro. However, the PRO driver provides a few features that Mesa still lacks, namely OpenGL compatibility profiles, OpenCL 2.0, and a fully conformant Vulkan implementation. Also, most of the games for which Mesa outperforms the closed-source driver run in Wine, rather than natively. Thus, the closed-source driver is mostly useful to users who want to play games (such as Civilization V) or use applications (such as UCSF Chimera) that rely on compatibility profiles, or want to run anything that uses Vulkan with advanced shaders, or want to fully exploit OpenCL.

<span class="label label-info">Info</span> **For most of the users so the amdgpu open source drivers are enough and work well for all the test we made.**

## AMDGPU

If you want to use the **amdgpu** open source drivers, all you have to do is install a Linux distribution. The amdgpu drivers are already included in the mainline Linux Kernel so they will be loaded by default at boot time.

<span class="label label-warning">Heads up!</span> Always remember to **keep updated** the kernel you are using to have the latest available fixes for performance and stability.


## AMDGPU-Pro

In order to download the latest stable updated version of the **AMDGPU-Pro drivers for the Ryzen&trade; v1000 Embedded Series processors** you can visit this page: [V-Series V1000 Drivers & Support | AMD ](https://www.amd.com/en/support/embedded/amd-ryzen-embedded-v-series-processors/v-series-v1000-radeon-vega-graphics).  

You can also reach this page from the standard [AMD Support page](https://www.amd.com/en/support) choosing the menu entries *Embedded -> AMD Ryzen&trade; Embedded V-series Processors -> V-Series V1000*.  

The OS supported by these drivers in the *Linux x86_64* version is **Ubuntu 18.04.1 LTS**.  

In the package you can find Documentation in the `doc` folder. Check the file `amdgpu_UserGuide.pdf` with the instructions to know how to install drivers.

<span class="label label-warning">Heads up!</span> We suggest to patiently read the amdgpu_UserGuide Documentation to properly install the drivers.

The easiest way to properly install the AMD drivers is by using all the pre-compiled packages (kernel and user-space) following the section *2.2 Installation Procedure for amdgpu from Debian Binaries*.  
You just need to run the `install_debs.sh` script that takes care of all the installations and setup needed.
Inside the package folder open a terminal and run the following commands:

      sudo chmod +x install_debs.sh
      sudo ./install_debs.sh

If you need, you will also find in the AMD package all the documentation and resources to compile the AMD kernel and user space packages on your own.  
