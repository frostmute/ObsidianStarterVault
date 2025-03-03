---
created: 2024-06-29
source: https://ubuntuforums.org/
category:
  - "[[Clippings]]"
cssclasses:
  - obsidian-banner
poster: "![poster]()"
---

![banner]()

```meta-bind-button
label: Fold All
icon: ""
hidden: false
class: ""
tooltip: ""
id: "001"
style: primary
actions:
  - type: command
    command: editor:fold-all

```

***

```cardlink
url: https://ubuntuforums.org/
title: "[SOLVED] Problems with Driver for Asus USB-AC53 Nano - Page 2"
description: 
host: ubuntuforums.org
image: 
```

-   [Forum](https://ubuntuforums.org/index.php)
-   [The Ubuntu Forum Community](https://ubuntuforums.org/forumdisplay.php?f=130)
-   [Ubuntu Official Flavours Support](https://ubuntuforums.org/forumdisplay.php?f=327)
-   [Networking & Wireless](https://ubuntuforums.org/forumdisplay.php?f=336)
-   \[SOLVED\] Problems with Driver for Asus USB-AC53 Nano

1.  ## Re: Problems with Driver for Asus USB-AC53 Nano
    
    > What version of Ubuntu are you using? I can get the module to compile with Ubuntu 16.04 with kernel 4.4.0-66 but it fails with the 4.8 kernels
    > 
    > I might have a fix
    > 
    > Code:
    > 
    > ```
    > cd Desktop
    > git clone https://github.com/jeremyb31/rtl8822bu.git
    > cd rtl8822bu
    > make clean
    > make
    > sudo make install
    > ```
    > 
    > Reboot
    
    > Last edited by jeremy31; June 2nd, 2017 at 11:16 AM.
    
2.  ## Re: Problems with Driver for Asus USB-AC53 Nano
    
    > Thank you so much for your help Jeremy!
    > 
    > I changed my kernel to 4.4.70, performed:
    > 
    > Code:
    > 
    > ```
    > make clean
    > make
    > sudo make install
    > modprobe 88x2bu
    > ```
    > 
    > and it compiled and installed without any problems at all. My wireless adapter immediately started working and I was able to connect to my wifi.
    > 
    > Thank you again so much for the help!
    > 
    > Hayden
    
3.  ## Re: Problems with Driver for Asus USB-AC53 Nano
    
    > I recently bought one of these and also had no problems when following the instructions. Thanks Jeremy!
    > 
    > I had a kernel upgrade recently. It appears I will have to compile and install after each new kernel, and it will no longer work when my 16.04 LTS updates to 18.04 LTS.
    > 
    > Is this correct?
    
4.  ## Re: Problems with Driver for Asus USB-AC53 Nano
    
    > Hi jeremy, sorry for bother you but I need your magic to fix a problem compiling your driver [https://github.com/jeremyb31/rtl8822bu](https://github.com/jeremyb31/rtl8822bu) for kernel 4.15
    > 
    > I've this error compiling it. Could you please help me? I'll pay you a beer  Many thanks!!
    > 
    > Code:
    > 
    > ```
    > ➜  Desktop git clone https://github.com/jeremyb31/rtl8822bu.gitcd rtl8822bu
    > make clean
    > make
    > sudo make install
    > Cloning into 'rtl8822bu'...
    > remote: Counting objects: 779, done.
    > remote: Total 779 (delta 0), reused 0 (delta 0), pack-reused 779
    > Receiving objects: 100% (779/779), 3.48 MiB | 2.60 MiB/s, done.
    > Resolving deltas: 100% (347/347), done.
    > make -C /lib/modules/4.15.0-22-generic/build M=/home/helektron/Desktop/rtl8822bu clean
    > make[1]: Entering directory '/usr/src/linux-headers-4.15.0-22-generic'
    > make[1]: Leaving directory '/usr/src/linux-headers-4.15.0-22-generic'
    > cd hal/phydm/ ; rm -fr */*.mod.c */*.mod */*.o */.*.cmd */*.ko
    > cd hal/phydm/ ; rm -fr *.mod.c *.mod *.o .*.cmd *.ko
    > cd hal/led ; rm -fr *.mod.c *.mod *.o .*.cmd *.ko
    > cd hal ; rm -fr */*/*.mod.c */*/*.mod */*/*.o */*/.*.cmd */*/*.ko
    > cd hal ; rm -fr */*.mod.c */*.mod */*.o */.*.cmd */*.ko
    > cd hal ; rm -fr *.mod.c *.mod *.o .*.cmd *.ko
    > cd core/efuse ; rm -fr *.mod.c *.mod *.o .*.cmd *.ko
    > cd core ; rm -fr *.mod.c *.mod *.o .*.cmd *.ko
    > cd os_dep/linux ; rm -fr *.mod.c *.mod *.o .*.cmd *.ko
    > cd os_dep ; rm -fr *.mod.c *.mod *.o .*.cmd *.ko
    > cd platform ; rm -fr *.mod.c *.mod *.o .*.cmd *.ko
    > rm -fr Module.symvers ; rm -fr Module.markers ; rm -fr modules.order
    > rm -fr *.mod.c *.mod *.o .*.cmd *.ko *~
    > rm -fr .tmp_versions
    > make ARCH=x86_64 CROSS_COMPILE= -C /lib/modules/4.15.0-22-generic/build M=/home/helektron/Desktop/rtl8822bu modules
    > make[1]: Entering directory '/usr/src/linux-headers-4.15.0-22-generic'
    >   CC [M]  /home/helektron/Desktop/rtl8822bu/core/rtw_cmd.o
    > In file included from /home/helektron/Desktop/rtl8822bu/include/osdep_service.h:41:0,
    >                  from /home/helektron/Desktop/rtl8822bu/include/drv_types.h:32,
    >                  from /home/helektron/Desktop/rtl8822bu/core/rtw_cmd.c:22:
    > /home/helektron/Desktop/rtl8822bu/include/osdep_service_linux.h: In function ‘_init_timer’:
    > /home/helektron/Desktop/rtl8822bu/include/osdep_service_linux.h:262:8: error: ‘_timer {aka struct timer_list}’ has no member named ‘data’
    >   ptimer-&gt;data = (unsigned long)cntx;
    >         ^~
    > /home/helektron/Desktop/rtl8822bu/include/osdep_service_linux.h:263:2: error: implicit declaration of function ‘init_timer’; did you mean ‘_init_timer’? [-Werror=implicit-function-declaration]
    >   init_timer(ptimer);
    >   ^~~~~~~~~~
    >   _init_timer
    > cc1: some warnings being treated as errors
    > scripts/Makefile.build:332: recipe for target '/home/helektron/Desktop/rtl8822bu/core/rtw_cmd.o' failed
    > make[2]: *** [/home/helektron/Desktop/rtl8822bu/core/rtw_cmd.o] Error 1
    > Makefile:1552: recipe for target '_module_/home/helektron/Desktop/rtl8822bu' failed
    > make[1]: *** [_module_/home/helektron/Desktop/rtl8822bu] Error 2
    > make[1]: Leaving directory '/usr/src/linux-headers-4.15.0-22-generic'
    > Makefile:1318: recipe for target 'modules' failed
    > make: *** [modules] Error 2
    > ```
    
5.  ## Re: Problems with Driver for Asus USB-AC53 Nano
    
    > Try [https://github.com/MeissnerEffect/rtl8822bu.git](https://github.com/MeissnerEffect/rtl8822bu.git) after doing a or delete the rtl8822bu directory from /home
    
6.  ## Re: Problems with Driver for Asus USB-AC53 Nano
    
    > All hail Jeremy. His fix works perfectly; I am using Kubuntu 16.04 with kernel 4.13.
    

#### Bookmarks

#### Posting Permissions
> make,ubuntu,fix,fails,4.8,kernels,git,sudo,install,reboot,clean,rtl8822bu,clone,https://github.com/jeremyb31/rtl8822bu.git,desktop,16.04,version,nano,usb-ac53,driver,asus,compile,problems,kernel,module,4.4.0-66