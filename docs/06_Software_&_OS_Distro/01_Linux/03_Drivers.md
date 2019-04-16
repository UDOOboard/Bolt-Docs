In order to download the latest stable updated version of the **AMD Ryzen&trade; drivers for the v1000 Embedded Series processors** you can visit this page: [V-Series V1000 Drivers & Support | AMD ](https://www.amd.com/en/support/embedded/amd-ryzen-embedded-v-series-processors/v-series-v1000).  
You can also reach this page from the standard [AMD Support page](https://www.amd.com/en/support) choosing the menu entries *Embedded -> AMD Ryzen&trade; Embedded V-series Processors -> V-Series V1000*.  
The OS supported by these drivers in the *Linux x86_64* version is **Ubuntu 18.04.1 LTS**.  

In the package you can find Documentation in the `doc` folder. Check the file `amdgpu_UserGuide.pdf` with the instructions to know how to install drivers.

<span class="label label-warning">Heads up!</span> We suggest to patiently read the amdgpu_UserGuide Documentation to properly install the drivers.

The easiest way to properly install the AMD drivers is by using all the pre-compiled packages (kernel and user-space) following the section *2.2 Installation Procedure for amdgpu from Debian Binaries*.  
You just need to run the `install_debs.sh` script that takes care of all the installations and setup needed.
Inside the package folder open a terminal and run the following commands:

      sudo chmod +x install_debs.sh
      sudo ./install_debs.sh

If you need, you will also find in the AMD package all the documentation and resources to compile the AMD kernel and user space packages by your own.  

You can also use the standard open source drivers contained in the Linux Kernel but some of the graphical features *(Libdrm, Mesa, Ddx, Gstomx, LLVM, Vulkan, ROCm)* may not work as expected.
