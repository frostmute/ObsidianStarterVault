---
created: 2024-06-29
source: https://forums.linuxmint.com/viewtopic.php?t=349313
category:
  - "[[../00 - CATEGORIES/Clippings]]"
cssclasses:
  - obsidian-banner
feature: "![[../03 - MEDIA & FILES/832dc7adaf726be47423e6804e1272e7_MD5.png]]"
---

![[.md|banner]]

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
url: https://forums.linuxmint.com/viewtopic.php?t=349313
title: "Asus AC53 Nano Driver - Linux Mint Forums"
description: "Forum rules
Before you post read how to get help. Topics in this forum are automatically closed 6 months after creation."
host: forums.linuxmint.com
image: 
```

**Forum rules**  
Before you post read [how to get help](https://forums.linuxmint.com/viewtopic.php?f=17&t=83444). Topics in this forum are automatically closed 6 months after creation.

**EclipseSSK**

### [[https://forums.linuxmint.com/viewtopic.php?p=2015999&sid=065fe03840b8e334f396bd2cd68401a2#p2015999]]

Hi, I just recently installed Linux for the first time. Chose Mint of course. I've been using this USB wireless dongle on windows. But I need to install the driver on Mint. I don't have access to ethernet, so I'll have to hop back into windows for files, if needed. I do have the CD that comes with the driver setup for Windows. There IS a Linux folder on the disk as well, so I believe I might already have what I need. But I don't really know exactly how to go about installing it. There are quite a few folders in the Linux folder on the disk.

Last edited by [LockBot](https://forums.linuxmint.com/memberlist.php?mode=viewprofile&u=338753&sid=065fe03840b8e334f396bd2cd68401a2) on Wed Dec 28, 2022 7:16 am, edited 1 time in total.  
**Reason:** _Topic automatically closed 6 months after creation. New replies are no longer allowed._

[![User avatar](../03%20-%20MEDIA%20&%20FILES/832dc7adaf726be47423e6804e1272e7_MD5.png)](https://forums.linuxmint.com/memberlist.php?mode=viewprofile&u=261886&sid=065fe03840b8e334f396bd2cd68401a2)

[spamegg](https://forums.linuxmint.com/memberlist.php?mode=viewprofile&u=261886&sid=065fe03840b8e334f396bd2cd68401a2)

Level 15  
![Level 15](../03%20-%20MEDIA%20&%20FILES/976a8f60a89b87046327c61858d1dd5f_MD5.gif "Level 15")

**Posts:** [5722](https://forums.linuxmint.com/search.php?author_id=261886&sr=posts&sid=065fe03840b8e334f396bd2cd68401a2)

**Joined:** Mon Oct 28, 2019 2:34 am

**Contact:**

### [[https://forums.linuxmint.com/viewtopic.php?p=2016023&sid=065fe03840b8e334f396bd2cd68401a2#p2016023]]

[[https://forums.linuxmint.com/viewtopic.php?p=2016023&sid=065fe03840b8e334f396bd2cd68401a2#p2016023 "Post"]] by **[spamegg](https://forums.linuxmint.com/memberlist.php?mode=viewprofile&u=261886&sid=065fe03840b8e334f396bd2cd68401a2)** » Sun May 16, 2021 1:55 am

Usually you don't need to install drivers on Linux and usually the hardware manufacturers (such as Asus) do not provide drivers for Linux. Is your dongle not working on Linux?

Please give us information about your install by entering this command in a terminal:

Click `</>` from the mini toolbar above the textbox where you type your reply  
and then place your cursor between the code markers and paste the results of the  
command between the code markers like this: `[code]Results[/code]`.

**EclipseSSK**

### [[https://forums.linuxmint.com/viewtopic.php?p=2016026&sid=065fe03840b8e334f396bd2cd68401a2#p2016026]]

[[https://forums.linuxmint.com/viewtopic.php?p=2016026&sid=065fe03840b8e334f396bd2cd68401a2#p2016026 "Post"]] by **EclipseSSK** » Sun May 16, 2021 2:03 am

Ok, I'll do that when I'm able to in a while. Got a 4 month old. But I did notice that in the network, there's a wired option but no wireless option. Is there a setting to turn on wireless that's stopping me?

**EclipseSSK**

### [[https://forums.linuxmint.com/viewtopic.php?p=2016077&sid=065fe03840b8e334f396bd2cd68401a2#p2016077]]

[[https://forums.linuxmint.com/viewtopic.php?p=2016077&sid=065fe03840b8e334f396bd2cd68401a2#p2016077 "Post"]] by **EclipseSSK** » Sun May 16, 2021 5:04 am

> [spamegg](https://forums.linuxmint.com/memberlist.php?mode=viewprofile&u=261886&sid=065fe03840b8e334f396bd2cd68401a2) wrote: [[https://forums.linuxmint.com/viewtopic.php?p=2016023&sid=065fe03840b8e334f396bd2cd68401a2#p2016023]]Sun May 16, 2021 1:55 am Usually you don't need to install drivers on Linux and usually the hardware manufacturers (such as Asus) do not provide drivers for Linux. Is your dongle not working on Linux?
> 
> Please give us information about your install by entering this command in a terminal:
> 
> Click `</>` from the mini toolbar above the textbox where you type your reply  
> and then place your cursor between the code markers and paste the results of the  
> command between the code markers like this: `[code]Results[/code]`.

`Eclipse@eclipse-Precision-T5600:~$ inxi -Fxpmrz   System:   Kernel: 5.4.0-58-generic x86_64 bits: 64 compiler: gcc v: 9.3.0   Desktop: Cinnamon 4.8.5 Distro: Linux Mint 20.1 Ulyssa   base: Ubuntu 20.04 focal   Machine:   Type: Desktop System: Dell product: Precision T5600 v: 01 serial: <filter>   Mobo: Dell model: 0Y56T3 v: A00 serial: <filter> BIOS: Dell v: A19   date: 06/30/2019   Memory:   RAM: total: 27.40 GiB used: 916.7 MiB (3.3%)   RAM Report:   permissions: Unable to run dmidecode. Root privileges required.   CPU:   Topology: 2x Quad Core model: Intel Xeon E5-2609 0 bits: 64 type: MCP SMP   arch: Sandy Bridge rev: 7 L2 cache: 20.0 MiB   flags: avx lm nx pae sse sse2 sse3 sse4_1 sse4_2 ssse3 vmx bogomips: 38320   Speed: 1197 MHz min/max: 1200/2400 MHz Core speeds (MHz): 1: 1197 2: 1197   3: 1197 4: 1197 5: 1197 6: 1197 7: 1197 8: 1197   Graphics:   Device-1: AMD Ellesmere [Radeon RX 470/480/570/570X/580/580X/590]   vendor: XFX Pine driver: amdgpu v: kernel bus ID: 06:00.0   Display: x11 server: X.Org 1.20.8 driver: amdgpu,ati   unloaded: fbdev,modesetting,vesa resolution: 3840x2160~30Hz   OpenGL: renderer: Radeon RX 570 Series (POLARIS10 DRM 3.35.0   5.4.0-58-generic LLVM 10.0.0)   v: 4.6 Mesa 20.0.8 direct render: Yes   Audio:   Device-1: Intel C600/X79 series High Definition Audio vendor: Dell   driver: snd_hda_intel v: kernel bus ID: 00:1b.0   Device-2: AMD Ellesmere HDMI Audio [Radeon RX 470/480 / 570/580/590]   vendor: XFX Pine driver: snd_hda_intel v: kernel bus ID: 06:00.1   Sound Server: ALSA v: k5.4.0-58-generic   `

[![User avatar](../03%20-%20MEDIA%20&%20FILES/993ce7ce7a9fbdcdac4d9a0339fd9383_MD5.png)](https://forums.linuxmint.com/memberlist.php?mode=viewprofile&u=235189&sid=065fe03840b8e334f396bd2cd68401a2)

[hglee](https://forums.linuxmint.com/memberlist.php?mode=viewprofile&u=235189&sid=065fe03840b8e334f396bd2cd68401a2)

Level 7  
![Level 7](../03%20-%20MEDIA%20&%20FILES/3f13a98f527e8438a1467857419d6c2f_MD5.gif "Level 7")

**Posts:** [1702](https://forums.linuxmint.com/search.php?author_id=235189&sr=posts&sid=065fe03840b8e334f396bd2cd68401a2)

**Joined:** Fri Jun 22, 2018 4:31 pm

### [[https://forums.linuxmint.com/viewtopic.php?p=2016332&sid=065fe03840b8e334f396bd2cd68401a2#p2016332]]

[[https://forums.linuxmint.com/viewtopic.php?p=2016332&sid=065fe03840b8e334f396bd2cd68401a2#p2016332 "Post"]] by **[hglee](https://forums.linuxmint.com/memberlist.php?mode=viewprofile&u=235189&sid=065fe03840b8e334f396bd2cd68401a2)** » Sun May 16, 2021 4:00 pm

> [EclipseSSK](https://forums.linuxmint.com/memberlist.php?mode=viewprofile&u=301907&sid=065fe03840b8e334f396bd2cd68401a2) wrote: [[https://forums.linuxmint.com/viewtopic.php?p=2015999&sid=065fe03840b8e334f396bd2cd68401a2#p2015999]]Sun May 16, 2021 12:32 am Hi, I just recently installed Linux for the first time. Chose Mint of course. I've been using this USB wireless dongle on windows. But I need to install the driver on Mint. I don't have access to ethernet, so I'll have to hop back into windows for files, if needed. I do have the CD that comes with the driver setup for Windows. There IS a Linux folder on the disk as well, so I believe I might already have what I need. But I don't really know exactly how to go about installing it. There are quite a few folders in the Linux folder on the disk.

Since you're dual-booting Windows, disable **Fast StartUp** in Windows power options. Also disable **Secure Boot** and **Fast Boot** in your BIOS. With Dell there might not be a Disabled option for Fast Boot, so select Minimal.

Those changes alone could fix your wifi problem.

If not, let's download and install a driver for the Asus AC53 dongle. With your T5600 online under Mint, via smartphone [tether](https://easylinuxtipsproject.blogspot.com/p/temporary-internet.html) or otherwise:

Open a Terminal window (Ctrl-Alt-T), then click CODE:SELECT ALL to copy-and-paste the following as one block of text, then tap _Enter_…

Code: [Select all](https://forums.linuxmint.com/viewtopic.php?t=349313#)

```
sudo apt-get install -y git build-essential dkms;cd ~/Downloads;M=rtl88x2bu;V=5.6.1;\
git clone https://github.com/cilynx/${M}.git;cd $M/;D=$M-$V;S=/usr/src;\
sudo mkdir -p $S/$D;sudo cp -r . $S/$D;sudo dkms install $M/$V;\
sudo modprobe 88x2bu;cd ~/Downloads;rm -rf $M;echo -e "\n\n\t... Done. Reboot! \n"
```

Reboot, when you see "… Done. Reboot!" in the Terminal.

Your Asus AC53 Nano should then be functional in Mint.

Linux Mint 21.3 Virginia, MATE 1.26.0, kernel 5.15.\*, **Dell** 2-in-1  
AMD **Ryzen 7** 5825U / Barcelo iGPU - 14" WUXGA Touchscreen  
MediaTek MT7921 WiFi-6 BT-5.2; 32GB DDR4@3200MHz; XPG 2TB-NVMe

**EclipseSSK**

### [[https://forums.linuxmint.com/viewtopic.php?p=2016440&sid=065fe03840b8e334f396bd2cd68401a2#p2016440]]

[[https://forums.linuxmint.com/viewtopic.php?p=2016440&sid=065fe03840b8e334f396bd2cd68401a2#p2016440 "Post"]] by **EclipseSSK** » Mon May 17, 2021 1:18 am

Is there a way I could use windows to copy that to a flash drive, put it on Linux, then run terminal? I'm completely new to this.

[![User avatar](../03%20-%20MEDIA%20&%20FILES/993ce7ce7a9fbdcdac4d9a0339fd9383_MD5.png)](https://forums.linuxmint.com/memberlist.php?mode=viewprofile&u=235189&sid=065fe03840b8e334f396bd2cd68401a2)

[hglee](https://forums.linuxmint.com/memberlist.php?mode=viewprofile&u=235189&sid=065fe03840b8e334f396bd2cd68401a2)

Level 7  
![Level 7](../03%20-%20MEDIA%20&%20FILES/3f13a98f527e8438a1467857419d6c2f_MD5.gif "Level 7")

**Posts:** [1702](https://forums.linuxmint.com/search.php?author_id=235189&sr=posts&sid=065fe03840b8e334f396bd2cd68401a2)

**Joined:** Fri Jun 22, 2018 4:31 pm

### [[https://forums.linuxmint.com/viewtopic.php?p=2016451&sid=065fe03840b8e334f396bd2cd68401a2#p2016451]]

[[https://forums.linuxmint.com/viewtopic.php?p=2016451&sid=065fe03840b8e334f396bd2cd68401a2#p2016451 "Post"]] by **[hglee](https://forums.linuxmint.com/memberlist.php?mode=viewprofile&u=235189&sid=065fe03840b8e334f396bd2cd68401a2)** » Mon May 17, 2021 3:04 am

> [EclipseSSK](https://forums.linuxmint.com/memberlist.php?mode=viewprofile&u=301907&sid=065fe03840b8e334f396bd2cd68401a2) wrote: [[https://forums.linuxmint.com/viewtopic.php?p=2016440&sid=065fe03840b8e334f396bd2cd68401a2#p2016440]]Mon May 17, 2021 1:18 am Is there a way I could use windows to copy that to a flash drive, put it on Linux, then run terminal? I'm completely new to this.

That process can be a royal pain because of potential **dependencies**, which are downloaded automatically with a web connection. Github provides source code, and building it to a module can require tools and code libraries that might not be included in a stock OS install. Even though most dependencies can be hunted down individually, it can become a time consuming process. Perhaps more than I'd want to volunteer here.

As a test, I installed Mint into a disposable VM. I had forgotten to not allow an Internet connection during the install, but you're past that point. When I got the driver source-code I was pleasantly surprised to have it compile without complaint. Yay for stock Mint including the basic kit for building kernel modules.

Here's the download link for the driver source-code file:  
`https://github.com/cilynx/rtl88x2bu/archive/refs/heads/5.6.1_30362.20181109_COEX20180928-6a6a.zip`

Depending on your download manager, the file will have one of these two names:

A) 5.6.1\_30362.20181109\_COEX20180928-6a6a.zip  
B) rtl88x2bu-5.6.1\_30362.20181109\_COEX20180928-6a6a.zip

When you get the file, put it into your Mint ~/Downloads folder, because that's where my install code will look. Then do this:

Open a Terminal (Ctrl-Alt-T), click CODE:SELECT ALL, then copy-and-paste the following as one block of text into the Terminal window…

Code: [Select all](https://forums.linuxmint.com/viewtopic.php?t=349313#)

```
cd ~/Downloads;M=rtl88x2bu;V=5.6.1;D=$M-$V;S=/usr/src;T=30362.20181109_COEX20180928-6a6a;\
N=${V}_${T}.zip;if [ ! -f "${N}" ];then N=${M}-${V}_${T}.zip;fi;Z=/dev/null;\
if [ -f "${N}" ];then unzip ${N}&gt;${Z};cd ${M}-${V}_${T};sudo mkdir -p ${S}/${D};\
sudo cp -r . ${S}/${D};sudo dkms install ${M}/${V};sudo modprobe 88x2bu;\
cd ~/Downloads;rm -rf ${M}-${V}_${T};echo -e "\n\n\t... Success. Reboot! \n\n";\
else echo -e "\n\n\t...FAIL: Source file not found...\n\n";fi
```

The _make_ step of the module build can take several moments, depending on your PC speed.

Reboot, when you see "… Success. Reboot!" in the Terminal.

With a little luck, your Asus AC53 will light up.

If you later wish to uninstall that RTL88x2BU driver: Open a Terminal window (Ctrl-Alt-T), and copy-and-paste the following command-line…

Code: [Select all](https://forums.linuxmint.com/viewtopic.php?t=349313#)

```
sudo dkms remove rtl88x2bu/5.6.1 --all
```

Last edited by [hglee](https://forums.linuxmint.com/memberlist.php?mode=viewprofile&u=235189&sid=065fe03840b8e334f396bd2cd68401a2) on Mon May 24, 2021 3:59 am, edited 7 times in total.

Linux Mint 21.3 Virginia, MATE 1.26.0, kernel 5.15.\*, **Dell** 2-in-1  
AMD **Ryzen 7** 5825U / Barcelo iGPU - 14" WUXGA Touchscreen  
MediaTek MT7921 WiFi-6 BT-5.2; 32GB DDR4@3200MHz; XPG 2TB-NVMe

**EclipseSSK**

### [[https://forums.linuxmint.com/viewtopic.php?p=2016463&sid=065fe03840b8e334f396bd2cd68401a2#p2016463]]

[[https://forums.linuxmint.com/viewtopic.php?p=2016463&sid=065fe03840b8e334f396bd2cd68401a2#p2016463 "Post"]] by **EclipseSSK** » Mon May 17, 2021 4:40 am

Couldn't locate dkms.conf file  
File: /usr/src/rtl88x2bu-5.6.1/dkms.conf does not exist

I'm in the directory and dkms.conf is there.

[![User avatar](../03%20-%20MEDIA%20&%20FILES/993ce7ce7a9fbdcdac4d9a0339fd9383_MD5.png)](https://forums.linuxmint.com/memberlist.php?mode=viewprofile&u=235189&sid=065fe03840b8e334f396bd2cd68401a2)

[hglee](https://forums.linuxmint.com/memberlist.php?mode=viewprofile&u=235189&sid=065fe03840b8e334f396bd2cd68401a2)

Level 7  
![Level 7](../03%20-%20MEDIA%20&%20FILES/3f13a98f527e8438a1467857419d6c2f_MD5.gif "Level 7")

**Posts:** [1702](https://forums.linuxmint.com/search.php?author_id=235189&sr=posts&sid=065fe03840b8e334f396bd2cd68401a2)

**Joined:** Fri Jun 22, 2018 4:31 pm

### [[https://forums.linuxmint.com/viewtopic.php?p=2016470&sid=065fe03840b8e334f396bd2cd68401a2#p2016470]]

[[https://forums.linuxmint.com/viewtopic.php?p=2016470&sid=065fe03840b8e334f396bd2cd68401a2#p2016470 "Post"]] by **[hglee](https://forums.linuxmint.com/memberlist.php?mode=viewprofile&u=235189&sid=065fe03840b8e334f396bd2cd68401a2)** » Mon May 17, 2021 5:10 am

> [EclipseSSK](https://forums.linuxmint.com/memberlist.php?mode=viewprofile&u=301907&sid=065fe03840b8e334f396bd2cd68401a2) wrote: [[https://forums.linuxmint.com/viewtopic.php?p=2016463&sid=065fe03840b8e334f396bd2cd68401a2#p2016463]]Mon May 17, 2021 4:40 am Couldn't locate dkms.conf file  
> File: /usr/src/rtl88x2bu-5.6.1/dkms.conf does not exist
> 
> I'm in the directory and dkms.conf is there.

I've run it multiple times. Are you sure about the file and folder?

Run the following to clear out whatever may have been loaded, using CODE:SELECT ALL to copy-and-paste into a Terminal window & tap _Enter_…

Code: [Select all](https://forums.linuxmint.com/viewtopic.php?t=349313#)

```
cd ~/Downloads;M=rtl88x2bu;V=5.6.1;D=$M-$V;S=/usr/src;T=30362.20181109_COEX20180928-6a6a;\
rm -rf ${M}-${V}_${T};sudo dkms remove ${M}/${V} --all;sudo rm -rf ${S}/${M}-${V}
```

I've edited my previous post, replacing the original instructions with code that will abort (showing "FAIL") if the required source file isn't present.

Go back up and run it again.

Last edited by [hglee](https://forums.linuxmint.com/memberlist.php?mode=viewprofile&u=235189&sid=065fe03840b8e334f396bd2cd68401a2) on Mon May 17, 2021 5:16 am, edited 1 time in total.

Linux Mint 21.3 Virginia, MATE 1.26.0, kernel 5.15.\*, **Dell** 2-in-1  
AMD **Ryzen 7** 5825U / Barcelo iGPU - 14" WUXGA Touchscreen  
MediaTek MT7921 WiFi-6 BT-5.2; 32GB DDR4@3200MHz; XPG 2TB-NVMe

[![User avatar](../03%20-%20MEDIA%20&%20FILES/993ce7ce7a9fbdcdac4d9a0339fd9383_MD5.png)](https://forums.linuxmint.com/memberlist.php?mode=viewprofile&u=235189&sid=065fe03840b8e334f396bd2cd68401a2)

[hglee](https://forums.linuxmint.com/memberlist.php?mode=viewprofile&u=235189&sid=065fe03840b8e334f396bd2cd68401a2)

Level 7  
![Level 7](../03%20-%20MEDIA%20&%20FILES/3f13a98f527e8438a1467857419d6c2f_MD5.gif "Level 7")

**Posts:** [1702](https://forums.linuxmint.com/search.php?author_id=235189&sr=posts&sid=065fe03840b8e334f396bd2cd68401a2)

**Joined:** Fri Jun 22, 2018 4:31 pm

### [[https://forums.linuxmint.com/viewtopic.php?p=2016473&sid=065fe03840b8e334f396bd2cd68401a2#p2016473]]

[[https://forums.linuxmint.com/viewtopic.php?p=2016473&sid=065fe03840b8e334f396bd2cd68401a2#p2016473 "Post"]] by **[hglee](https://forums.linuxmint.com/memberlist.php?mode=viewprofile&u=235189&sid=065fe03840b8e334f396bd2cd68401a2)** » Mon May 17, 2021 5:27 am

> [EclipseSSK](https://forums.linuxmint.com/memberlist.php?mode=viewprofile&u=301907&sid=065fe03840b8e334f396bd2cd68401a2) wrote: [[https://forums.linuxmint.com/viewtopic.php?p=2016471&sid=065fe03840b8e334f396bd2cd68401a2#p2016471]]Mon May 17, 2021 5:13 am I ran the wrong code…my bad

No worries.

I usually provide code that will undo whatever my Terminal instructions do. Now you have that, in my previous post.

Do tell how your AC53 is behaving.

Linux Mint 21.3 Virginia, MATE 1.26.0, kernel 5.15.\*, **Dell** 2-in-1  
AMD **Ryzen 7** 5825U / Barcelo iGPU - 14" WUXGA Touchscreen  
MediaTek MT7921 WiFi-6 BT-5.2; 32GB DDR4@3200MHz; XPG 2TB-NVMe

**EclipseSSK**

### [[https://forums.linuxmint.com/viewtopic.php?p=2016476&sid=065fe03840b8e334f396bd2cd68401a2#p2016476]]

[[https://forums.linuxmint.com/viewtopic.php?p=2016476&sid=065fe03840b8e334f396bd2cd68401a2#p2016476 "Post"]] by **EclipseSSK** » Mon May 17, 2021 5:32 am

> [hglee](https://forums.linuxmint.com/memberlist.php?mode=viewprofile&u=235189&sid=065fe03840b8e334f396bd2cd68401a2) wrote: [[https://forums.linuxmint.com/viewtopic.php?p=2016470&sid=065fe03840b8e334f396bd2cd68401a2#p2016470]]Mon May 17, 2021 5:10 am
> 
> > [EclipseSSK](https://forums.linuxmint.com/memberlist.php?mode=viewprofile&u=301907&sid=065fe03840b8e334f396bd2cd68401a2) wrote: [[https://forums.linuxmint.com/viewtopic.php?p=2016463&sid=065fe03840b8e334f396bd2cd68401a2#p2016463]]Mon May 17, 2021 4:40 am Couldn't locate dkms.conf file  
> > File: /usr/src/rtl88x2bu-5.6.1/dkms.conf does not exist
> > 
> > I'm in the directory and dkms.conf is there.
> 
> I've run it multiple times. Are you sure about the file and folder?
> 
> Run the following to clear out whatever may have been loaded, using CODE:SELECT ALL to copy-and-paste into a Terminal window & tap _Enter_…
> 
> Code: [Select all](https://forums.linuxmint.com/viewtopic.php?t=349313#)
> 
> ```
> cd ~/Downloads;M=rtl88x2bu;V=5.6.1;D=$M-$V;S=/usr/src;T=30362.20181109_COEX20180928-6a6a;\
> rm -rf ${M}-${V}_${T};sudo dkms remove ${M}/${V} --all;sudo rm -rf ${S}/${M}-${V}
> ```
> 
> I've edited my previous post, replacing the original instructions with code that will abort (showing "FAIL") if the required source file isn't present.
> 
> Go back up and run it again.

Ok, I have the ZIP in the downloads directory. What commands do I run again? The last one failed because of the missing source file as you said. But I don't know which updated command you mean to use after your edit.

[![User avatar](../03%20-%20MEDIA%20&%20FILES/993ce7ce7a9fbdcdac4d9a0339fd9383_MD5.png)](https://forums.linuxmint.com/memberlist.php?mode=viewprofile&u=235189&sid=065fe03840b8e334f396bd2cd68401a2)

[hglee](https://forums.linuxmint.com/memberlist.php?mode=viewprofile&u=235189&sid=065fe03840b8e334f396bd2cd68401a2)

Level 7  
![Level 7](../03%20-%20MEDIA%20&%20FILES/3f13a98f527e8438a1467857419d6c2f_MD5.gif "Level 7")

**Posts:** [1702](https://forums.linuxmint.com/search.php?author_id=235189&sr=posts&sid=065fe03840b8e334f396bd2cd68401a2)

**Joined:** Fri Jun 22, 2018 4:31 pm

### [[https://forums.linuxmint.com/viewtopic.php?p=2016481&sid=065fe03840b8e334f396bd2cd68401a2#p2016481]]

[[https://forums.linuxmint.com/viewtopic.php?p=2016481&sid=065fe03840b8e334f396bd2cd68401a2#p2016481 "Post"]] by **[hglee](https://forums.linuxmint.com/memberlist.php?mode=viewprofile&u=235189&sid=065fe03840b8e334f396bd2cd68401a2)** » Mon May 17, 2021 5:48 am

> [EclipseSSK](https://forums.linuxmint.com/memberlist.php?mode=viewprofile&u=301907&sid=065fe03840b8e334f396bd2cd68401a2) wrote: [[https://forums.linuxmint.com/viewtopic.php?p=2016476&sid=065fe03840b8e334f396bd2cd68401a2#p2016476]]Mon May 17, 2021 5:32 am Ok, I have the ZIP in the downloads directory. What commands do I run again? The last one failed because of the missing source file as you said. But I don't know which updated command you mean to use after your edit.

Since a previous attempt may have partially completed, we'll first remove whatever bits remain:

Open a Terminal (Ctrl-Alt-T), click CODE:SELECT ALL, then copy-and-paste the following as one block of text into the Terminal window…

Code: [Select all](https://forums.linuxmint.com/viewtopic.php?t=349313#)

```
cd ~/Downloads;M=rtl88x2bu;V=5.6.1;D=$M-$V;S=/usr/src;T=30362.20181109_COEX20180928-6a6a;\
rm -rf ${M}-${V}_${T};sudo dkms remove ${M}/${V} --all;sudo rm -rf ${S}/${M}-${V}
```

It's okay if you see some error messages.

Now build and install the driver, with the source zip file in your ~/Downloads folder:

Open a Terminal (Ctrl-Alt-T), click CODE:SELECT ALL, then copy-and-paste the following as one block of text into the Terminal window…

Code: [Select all](https://forums.linuxmint.com/viewtopic.php?t=349313#)

```
cd ~/Downloads;M=rtl88x2bu;V=5.6.1;D=$M-$V;S=/usr/src;T=30362.20181109_COEX20180928-6a6a;\
N=${V}_${T}.zip;if [ ! -f "${N}" ];then N=${M}-${V}_${T}.zip;fi;Z=/dev/null;\
if [ -f "${N}" ];then unzip ${N}&gt;${Z};cd ${M}-${V}_${T};sudo mkdir -p ${S}/${D};\
sudo cp -r . ${S}/${D};sudo dkms install ${M}/${V};sudo modprobe 88x2bu;\
cd ~/Downloads;rm -rf ${M}-${V}_${T};echo -e "\n\n\t... Success. Reboot! \n\n";\
else echo -e "\n\n\t...FAIL: Source file not found...\n\n";fi
```

The _make_ step of the module build can take several moments, depending on your PC speed.

The entire procedure will abort (you'll see "FAIL" in the Terminal) if the required source file isn't where it should be.

Reboot, when you see "… Success. Reboot!" in the Terminal.

Last edited by [hglee](https://forums.linuxmint.com/memberlist.php?mode=viewprofile&u=235189&sid=065fe03840b8e334f396bd2cd68401a2) on Mon May 24, 2021 9:47 am, edited 3 times in total.

Linux Mint 21.3 Virginia, MATE 1.26.0, kernel 5.15.\*, **Dell** 2-in-1  
AMD **Ryzen 7** 5825U / Barcelo iGPU - 14" WUXGA Touchscreen  
MediaTek MT7921 WiFi-6 BT-5.2; 32GB DDR4@3200MHz; XPG 2TB-NVMe

[![User avatar](../03%20-%20MEDIA%20&%20FILES/993ce7ce7a9fbdcdac4d9a0339fd9383_MD5.png)](https://forums.linuxmint.com/memberlist.php?mode=viewprofile&u=235189&sid=065fe03840b8e334f396bd2cd68401a2)

[hglee](https://forums.linuxmint.com/memberlist.php?mode=viewprofile&u=235189&sid=065fe03840b8e334f396bd2cd68401a2)

Level 7  
![Level 7](../03%20-%20MEDIA%20&%20FILES/3f13a98f527e8438a1467857419d6c2f_MD5.gif "Level 7")

**Posts:** [1702](https://forums.linuxmint.com/search.php?author_id=235189&sr=posts&sid=065fe03840b8e334f396bd2cd68401a2)

**Joined:** Fri Jun 22, 2018 4:31 pm

### [[https://forums.linuxmint.com/viewtopic.php?p=2016517&sid=065fe03840b8e334f396bd2cd68401a2#p2016517]]

[[https://forums.linuxmint.com/viewtopic.php?p=2016517&sid=065fe03840b8e334f396bd2cd68401a2#p2016517 "Post"]] by **[hglee](https://forums.linuxmint.com/memberlist.php?mode=viewprofile&u=235189&sid=065fe03840b8e334f396bd2cd68401a2)** » Mon May 17, 2021 7:07 am

> [EclipseSSK](https://forums.linuxmint.com/memberlist.php?mode=viewprofile&u=301907&sid=065fe03840b8e334f396bd2cd68401a2) wrote: [[https://forums.linuxmint.com/viewtopic.php?p=2016491&sid=065fe03840b8e334f396bd2cd68401a2#p2016491]]Mon May 17, 2021 6:20 am I'm still getting source file error

Aha, I've discovered a **sneaky quirk** that can happen when downloading a file from Github: The name of the file that you receive may depend upon the download manager that you use -- even though the download link is identical in each case.

In this case, the download link is as I noted earlier:  
`https://github.com/cilynx/rtl88x2bu/archive/refs/heads/5.6.1_30362.20181109_COEX20180928-6a6a.zip`

When I use the **wget** utility to download with that link, the file I receive is named 5.6.1\_30362.20181109\_COEX20180928-6a6a.zip.

However, when I use Firefox with that very same download link, the file is named rtl88x2bu-5.6.1\_30362.20181109\_COEX20180928-6a6a.zip!

My code was looking for that first file name. The other name would cause a fail.

So, I've modified my install code again: It will now seek and accept either of those file names, and abort only if neither is found. I've gone back and edited my previous posts, to insert the new instructions.

Just go back up to [[https://forums.linuxmint.com/viewtopic.php?p=2016481#p2016481]] and start over.

[Feelin' Lucky](https://www.youtube.com/watch?v=THHBANUWzD4)? ![;)](../03%20-%20MEDIA%20&%20FILES/86a4f29ea297611acdf0753792fab9a0_MD5.gif "Wink")

Linux Mint 21.3 Virginia, MATE 1.26.0, kernel 5.15.\*, **Dell** 2-in-1  
AMD **Ryzen 7** 5825U / Barcelo iGPU - 14" WUXGA Touchscreen  
MediaTek MT7921 WiFi-6 BT-5.2; 32GB DDR4@3200MHz; XPG 2TB-NVMe

**EclipseSSK**

### [[https://forums.linuxmint.com/viewtopic.php?p=2016526&sid=065fe03840b8e334f396bd2cd68401a2#p2016526]]

[[https://forums.linuxmint.com/viewtopic.php?p=2016526&sid=065fe03840b8e334f396bd2cd68401a2#p2016526 "Post"]] by **EclipseSSK** » Mon May 17, 2021 7:23 am

Ah, I used IDM. The driver did install, but still no wifi option. I will mention again that the CD that came with the wifi adapter does have a Linux folder inside, a long with Mac and Windows. It appears to be v5.6.1.5. I have that zip folder. I'll just write it out.

rtl88x2BU\_WiFi\_linux\_v5.6.1.5\_33902.20190604\_COEX20180928-6a6a.tar.gz

I added it to Git. Sorry if I did it the wrong way.

[https://github.com/EclipseSSK/Asus-AC53-Nano-Linux](https://github.com/EclipseSSK/Asus-AC53-Nano-Linux)

[![User avatar](../03%20-%20MEDIA%20&%20FILES/993ce7ce7a9fbdcdac4d9a0339fd9383_MD5.png)](https://forums.linuxmint.com/memberlist.php?mode=viewprofile&u=235189&sid=065fe03840b8e334f396bd2cd68401a2)

[hglee](https://forums.linuxmint.com/memberlist.php?mode=viewprofile&u=235189&sid=065fe03840b8e334f396bd2cd68401a2)

Level 7  
![Level 7](../03%20-%20MEDIA%20&%20FILES/3f13a98f527e8438a1467857419d6c2f_MD5.gif "Level 7")

**Posts:** [1702](https://forums.linuxmint.com/search.php?author_id=235189&sr=posts&sid=065fe03840b8e334f396bd2cd68401a2)

**Joined:** Fri Jun 22, 2018 4:31 pm

### [[https://forums.linuxmint.com/viewtopic.php?p=2016604&sid=065fe03840b8e334f396bd2cd68401a2#p2016604]]

[[https://forums.linuxmint.com/viewtopic.php?p=2016604&sid=065fe03840b8e334f396bd2cd68401a2#p2016604 "Post"]] by **[hglee](https://forums.linuxmint.com/memberlist.php?mode=viewprofile&u=235189&sid=065fe03840b8e334f396bd2cd68401a2)** » Mon May 17, 2021 10:40 am

> [EclipseSSK](https://forums.linuxmint.com/memberlist.php?mode=viewprofile&u=301907&sid=065fe03840b8e334f396bd2cd68401a2) wrote: [[https://forums.linuxmint.com/viewtopic.php?p=2016526&sid=065fe03840b8e334f396bd2cd68401a2#p2016526]]Mon May 17, 2021 7:23 am Ah, I used IDM. The driver did install, but still no wifi option. I will mention again that the CD that came with the wifi adapter does have a Linux folder inside, a long with Mac and Windows. It appears to be v5.6.1.5. I have that zip folder. I'll just write it out.
> 
> rtl88x2BU\_WiFi\_linux\_v5.6.1.5\_33902.20190604\_COEX20180928-6a6a.tar.gz
> 
> I added it to Git. Sorry if I did it the wrong way.
> 
> [https://github.com/EclipseSSK/Asus-AC53-Nano-Linux](https://github.com/EclipseSSK/Asus-AC53-Nano-Linux)

That file name suggests it's from the same programmer, **cilynx**, with just a minor update. Though its source files aren't configured to automatically rebuild and re-install whenever you have kernel updates.

There is another wifi driver you can install without dependencies.

Before installing some other driver, remove the one you previously installed:

Open a Terminal (Ctrl-Alt-T), click CODE:SELECT ALL, then copy-and-paste the following as one block of text into the Terminal window…

Code: [Select all](https://forums.linuxmint.com/viewtopic.php?t=349313#)

```
cd ~/Downloads;N=88x2bu;M=rtl$N;V=5.6.1;D=$M-$V;S=/usr/src;T=30362.20181109_COEX20180928-6a6a;\
rm -rf ${D}_${T};sudo dkms remove ${M}/${V} --all;sudo rm -rf ${S}/${D};sudo modprobe -r ${N}
```

It's okay if you see some error messages.

The download link for the other driver source file is:  
`https://github.com/jeremyb31/rtl8822bu/archive/refs/heads/master.zip`  
The file name will be either rt8822bu-master.zip or just master.zip. Put it in your Mint ~/Downloads folder.

Build and install that driver:

Open a Terminal (Ctrl-Alt-T), click CODE:SELECT ALL, then copy-and-paste the following as one block of text into the Terminal window…

Code: [Select all](https://forums.linuxmint.com/viewtopic.php?t=349313#)

```
cd ~/Downloads;N=8822bu;M=rtl$N;V=1.1;D=$N-$V;T=master;E=$M-$T;P=${E}.zip;S=/usr/src;\
if [ ! -f "${P}" ];then P=${T}.zip;fi;if [ -f "${P}" ];then unzip ${P}&gt;/dev/null;\
cd ${E};sudo mkdir -p ${S}/${D};sudo cp -r . ${S}/${D};sudo dkms install ${N}/${V};\
sudo modprobe ${N};cd ~/Downloads;rm -rf ${E};echo -e "\n\n\t... Success. Reboot. \n\n";\
else echo -e "\n\n\t...FAIL: Source file not found...\n\n";fi
```

The _make_ step of the module build can take several moments, depending on your PC speed.

The entire procedure will abort (you'll see "FAIL" in the Terminal) if the required source file isn't where it should be.

Reboot, when you see "… Success. Reboot." in the Terminal.

If you later wish to remove this wifi driver: Use CODE:SELECT ALL to copy-and-paste the following into a Terminal window…

Code: [Select all](https://forums.linuxmint.com/viewtopic.php?t=349313#)

```
cd ~/Downloads;N=8822bu;M=rtl$N;V=1.1;D=$N-$V;S=/usr/src;T=master;rm -rf ${M}-${T};\
sudo dkms remove ${N}/${V} --all;sudo rm -rf ${S}/${D};sudo modprobe -r ${N};echo -e "\n\t... Reboot ...\n"
```

Last edited by [hglee](https://forums.linuxmint.com/memberlist.php?mode=viewprofile&u=235189&sid=065fe03840b8e334f396bd2cd68401a2) on Mon May 24, 2021 9:58 am, edited 1 time in total.

Linux Mint 21.3 Virginia, MATE 1.26.0, kernel 5.15.\*, **Dell** 2-in-1  
AMD **Ryzen 7** 5825U / Barcelo iGPU - 14" WUXGA Touchscreen  
MediaTek MT7921 WiFi-6 BT-5.2; 32GB DDR4@3200MHz; XPG 2TB-NVMe

**EclipseSSK**

### [[https://forums.linuxmint.com/viewtopic.php?p=2016813&sid=065fe03840b8e334f396bd2cd68401a2#p2016813]]

[[https://forums.linuxmint.com/viewtopic.php?p=2016813&sid=065fe03840b8e334f396bd2cd68401a2#p2016813 "Post"]] by **EclipseSSK** » Mon May 17, 2021 7:28 pm

Apparently I had already installed the driver but still no wifi. The USB ports are working, but it's just not seeing it for some reason.

[![User avatar](../03%20-%20MEDIA%20&%20FILES/993ce7ce7a9fbdcdac4d9a0339fd9383_MD5.png)](https://forums.linuxmint.com/memberlist.php?mode=viewprofile&u=235189&sid=065fe03840b8e334f396bd2cd68401a2)

[hglee](https://forums.linuxmint.com/memberlist.php?mode=viewprofile&u=235189&sid=065fe03840b8e334f396bd2cd68401a2)

Level 7  
![Level 7](../03%20-%20MEDIA%20&%20FILES/3f13a98f527e8438a1467857419d6c2f_MD5.gif "Level 7")

**Posts:** [1702](https://forums.linuxmint.com/search.php?author_id=235189&sr=posts&sid=065fe03840b8e334f396bd2cd68401a2)

**Joined:** Fri Jun 22, 2018 4:31 pm

### [[https://forums.linuxmint.com/viewtopic.php?p=2016819&sid=065fe03840b8e334f396bd2cd68401a2#p2016819]]

[[https://forums.linuxmint.com/viewtopic.php?p=2016819&sid=065fe03840b8e334f396bd2cd68401a2#p2016819 "Post"]] by **[hglee](https://forums.linuxmint.com/memberlist.php?mode=viewprofile&u=235189&sid=065fe03840b8e334f396bd2cd68401a2)** » Mon May 17, 2021 7:49 pm

> [EclipseSSK](https://forums.linuxmint.com/memberlist.php?mode=viewprofile&u=301907&sid=065fe03840b8e334f396bd2cd68401a2) wrote: [[https://forums.linuxmint.com/viewtopic.php?p=2016813&sid=065fe03840b8e334f396bd2cd68401a2#p2016813]]Mon May 17, 2021 7:28 pm Apparently I had already installed the driver but still no wifi. The USB ports are working, but it's just not seeing it for some reason.

So you've tried the two different driver builds, from two different sources, that I've posted here?

Linux Mint 21.3 Virginia, MATE 1.26.0, kernel 5.15.\*, **Dell** 2-in-1  
AMD **Ryzen 7** 5825U / Barcelo iGPU - 14" WUXGA Touchscreen  
MediaTek MT7921 WiFi-6 BT-5.2; 32GB DDR4@3200MHz; XPG 2TB-NVMe

**EclipseSSK**

### [[https://forums.linuxmint.com/viewtopic.php?p=2016822&sid=065fe03840b8e334f396bd2cd68401a2#p2016822]]

[[https://forums.linuxmint.com/viewtopic.php?p=2016822&sid=065fe03840b8e334f396bd2cd68401a2#p2016822 "Post"]] by **EclipseSSK** » Mon May 17, 2021 8:01 pm

Yes, still no change. Blue light on wireless adapter still not on.
