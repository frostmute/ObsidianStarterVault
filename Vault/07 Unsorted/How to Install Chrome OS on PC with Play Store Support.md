---
banner: https://i.pcmag.com/imagery/reviews/05cAYKK7zk3e4e9cS9FFEn0-82.fit_lim.size_1050x591.v1701290726.png
cssclasses:
  - dashboard
feature: "![[03 MEDIA & FILES/rufus.jpg]]"
---

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

## Install Chrome OS on PC with Play Store Support (2022)

Before we start our tutorial, let’s get the requirements and downloads out of the way. Once you meet all the requirements and download the relevant files, the setup will go smoothly. You can click on the links below to move between different menus.

### Requirements for Installing Chrome OS on Windows PC

- UEFI support in the motherboard
- Support for legacy BIOS has also been added, but there are a few limitations. You can read the documentation [[https://github.com/sebanc/brunch/blob/master/README.md#limited-support-for-mbrbios-devices]].
- Intel-based CPU and GPU
- Support for AMD CPU and GPU has also been added, but currently, it only supports AMD Ryzen 3XXX and AMD Stoney Ridge processors
- A USB flash drive with at least 16GB of storage space

### Install Chrome OS on Windows: Required Downloads

1. First off, download the [Linux Mint Cinnamon](https://www.linuxmint.com/download.php) image. You can also use other Linux distros such as Ubuntu or Debian, but since **Linux Mint is pretty lightweight**, I am using it in this tutorial.

![[Updated February 2021|[Updated February 2021|[Updated February 2021|[Updated February 2021)](03 MEDIA & FILES/Install_Chrome_OS_on_PC_with_Play_Store_Support_(Updated_February_2021|Install Chrome OS on PC with Play Store Support (Updated February 2021|[Updated February 2021|[Updated February 2021|[Updated February 2021)]]]]]]-2.jpg)

2. Next, **download Rufus** ([Free](https://rufus.ie/)) so that we can flash Linux Mint Cinnamon on the USB drive.

![[03 MEDIA & FILES/rufus.jpg|rufus]]

3. After that, download the official Chrome OS recovery image from [here](https://cros-updates-serving.appspot.com/). If this link is not working then you can download the image from [here as well](https://cros.tech/). Open the website and search for “rammus”. Now, click on the latest recovery image to download it (right now it’s 87, but it may change in the future). Here, I am recommending “rammus” because it works on modern Intel processors. However, you should **follow the below rule** and download the specific image based on your processor.

- “rammus” is the recommended image for devices with 4th generation Intel CPU and newer.
- “samus” is the recommended image for devices with 3rd generation Intel CPU and older.
- “zork” is the image to use for AMD Ryzen 3XXX.
- “grunt” is the image to use for AMD Stoney Ridge.

![[Updated February 2021|[Updated February 2021|[Updated February 2021|[Updated February 2021)](03 MEDIA & FILES/Install_Chrome_OS_on_PC_with_Play_Store_Support_(Updated_February_2021|Install Chrome OS on PC with Play Store Support (Updated February 2021|[Updated February 2021|[Updated February 2021|[Updated February 2021)]]]]]].jpg)

4. Now, download the most important file: Brunch. It’s a framework built by a developer named [sebanc](https://github.com/sebanc) so huge thanks to him for making this project possible. **The framework creates a generic Chrome OS image** from the official recovery image so it can be installed on any Windows PC. To download the file, [click here](https://github.com/sebanc/brunch/releases) and look for the latest stable build and then click on “Assets”. Now, download the “tar.gz” file.

![[Updated February 2021|[Updated February 2021|[Updated February 2021|[Updated February 2021)](03 MEDIA & FILES/Install_Chrome_OS_on_PC_with_Play_Store_Support_(Updated_February_2021|Install Chrome OS on PC with Play Store Support (Updated February 2021|[Updated February 2021|[Updated February 2021|[Updated February 2021)]]]]]]-2.jpg)

5. Finally, download the “install.sh” script which magically **installs Chrome OS without manually typing the commands**. The script has been written by Kedar Nimbalkar. To download it, [click here](https://raw.githubusercontent.com/shrikant2002/ChromeOS/master/install.sh) and press Ctrl + S to save the file. If the above link is not working then you can click on this [alternative link](https://drive.google.com/file/d/17VMmDm_4IBdGU2p4cBKxhQY_pH0rr5rV/view?usp=sharing) to download the “install.sh” script.

Now that we are done with the downloads, let’s jump to the steps, shall we?

![[03 MEDIA & FILES/Install_Chrome_OS_on_PC_with_Play_Store_Support-2.jpg|Install Chrome OS on PC with Play Store Support]]

### Install Chrome OS on PC with Play Store Support

Before moving to installation steps, I want to give a quick rundown as to how we will install Chrome OS on PC with Play Store support. First off, we will boot Linux Mint through the USB drive on our Windows computer, and from there, we can run the script and install Chrome OS on our PC. Keep in mind, this process **will completely wipe your hard drive including personal files and folders**. So create a backup before you proceed. With that out of the way, let’s move to the steps.

### Flash and Manage Files

1. Connect your USB flash drive and open Rufus. Next, click on the “Select” button and **choose the Linux Mint Cinnamon image**. Now, just click on “Start”. You will get a few prompts so click on “Yes” and “OK” to continue the flashing process.

![[03 MEDIA & FILES/Install_Chrome_OS_on_PC_with_Play_Store_Support-1.jpg|Install Chrome OS on PC with Play Store Support]]

2. After Rufus is done with flashing, close it. Now, **create a folder named “Chrome OS” on your desktop**. Move the “install.sh” file to the “Chrome OS” folder.

![[03 MEDIA & FILES/Flash_and_Move_the_Files-1.jpg|Flash and Move the Files]]

3. Next, right-click on the Brunch file and **choose “Extract to Brunch…”**. All the files will be extracted in a folder on the desktop.

![[03 MEDIA & FILES/Install_Chrome_OS_on_PC_with_Play_Store_Support-1.jpg|Install Chrome OS on PC with Play Store Support]]

4. Now, move all the extracted Brunch files to the **same “Chrome OS” folder** on the desktop.

![[03 MEDIA & FILES/Flash_and_Move_the_Files-1.jpg|Flash and Move the Files]]

5. Similarly, extract the official Chrome OS recovery image and you will get a folder on the desktop. Open it and **rename the file** to `rammus_recovery.bin`. If you have downloaded another image then rename it accordingly. For example, if you have downloaded the “samus” image then rename it to `samus_recovery.bin`.

![[03 MEDIA & FILES/Install_Chrome_OS_on_PC_with_Play_Store_Support-1.jpg|Install Chrome OS on PC with Play Store Support]]

6. Finally, **move the “rammus_recovery.bin” file** to the “Chrome OS” folder. By the end, you should have these 6 files inside the “Chrome OS” folder.

![[03 MEDIA & FILES/Flash_and_Move_the_Files.jpg|Flash and Move the Files]]

7. Now, **move the whole “Chrome OS” folder** to the USB drive on which you just flashed Linux Mint Cinnamon.

![[03 MEDIA & FILES/Install_Chrome_OS_on_PC_with_Play_Store_Support-1.jpg|Install Chrome OS on PC with Play Store Support]]

### Boot into Linux Mint Cinnamon

1. **Plug the USB flash drive** into the PC on which you want to install Chrome OS. If you are installing Chrome OS on the same PC then keep it plugged in.

2. Next, restart your PC and **press the boot key continuously** to boot into the UEFI/BIOS menu. If you don’t know the boot key of your PC then you can find it from the below table.

![[03 MEDIA & FILES/Install_Chrome_OS_on_PC_with_Play_Store_Support-2.jpg|Install Chrome OS on PC with Play Store Support]]

3. Once you have entered the BIOS, move to the “Boot” tab and **select “UEFI”** from the Boot List Option. If this option is not available then don’t worry, move to the next step.

![[03 MEDIA & FILES/Install_Chrome_OS_on_PC_with_Play_Store_Support-2.jpg|Install Chrome OS on PC with Play Store Support]]

4. After that, move to the “Security” tab and **disable “Secure Boot”**. Keep in mind, every BIOS has its own interface so the menu placement might differ from one PC to another. Nevertheless, look for “UEFI” and “Secure Boot” under Security, Boot, or System Configuration tabs and makes the changes accordingly. Keep in mind, disabling Secure Boot is mandatory.

![[03 MEDIA & FILES/How_to_Install_Chrome_OS_on_PC_with_Play_Store_Support.jpg|How to Install Chrome OS on PC with Play Store Support]]

5. Finally, move to the “Exit” tab and choose “**Exit Save Changes**“. Immediately, after that, start pressing the boot key again. You will be asked to choose your boot device. Select the “USB drive” and hit enter.

![[03 MEDIA & FILES/Install_Chrome_OS_on_PC_with_Play_Store_Support-2.jpg|Install Chrome OS on PC with Play Store Support]]

6. You will boot straight into Linux Mint Cinnamon. If you are prompted with a splash screen, choose the default option: “**Start Linux Mint**“.

![[03 MEDIA & FILES/Install_Chrome_OS_on_PC.jpg|Install Chrome OS on PC]]

### Install Chrome OS on PC

1. Now that you have booted into Linux Mint, click on the network icon at the bottom-right corner and **connect to WiFi or Ethernet**. The Chrome OS installer will need an active internet connection to download some missing libraries and dependencies.

![[03 MEDIA & FILES/Install_Chrome_OS_on_PC_with_Play_Store_Support-2.jpg|Install Chrome OS on PC with Play Store Support]]

2. After that, open the “Home” folder on the desktop and **move to the “File System”** tab.

![[03 MEDIA & FILES/Install_Chrome_OS_on_PC_with_Play_Store_Support-2.jpg|Install Chrome OS on PC with Play Store Support]]

3. Here, click on the search button and **type “Chrome OS”** to find the folder that we moved earlier.

![[03 MEDIA & FILES/Install_Chrome_OS.jpg|Install Chrome OS]]

4. Now, open the folder and right-click inside the folder to **open the Terminal**. Here, type `sudo sh install.sh` and hit enter. It will start downloading some libraries and dependencies.

![[03 MEDIA & FILES/Install_Chrome_OS_on_PC_with_Play_Store_Support-1.jpg|Install Chrome OS on PC with Play Store Support]]

5. After a while, it will ask if you want to continue with the installation. Keep in mind, **this will completely wipe your whole hard drive**. To proceed with the installation, type `yes` and hit enter. It will now start installing Chrome OS on your PC.

_**Note:** If you get any syntax error during installation then move to the Troubleshoot section below to find the solution._

![[03 MEDIA & FILES/install_chrome_os_on_pc.jpg|install chrome os on pc]]

6. After the installation is done, open the start menu of Linux Mint located at the bottom-left corner and click on the “Turn off” button. Here, **choose “Shut Down”** to turn off your PC.

![[03 MEDIA & FILES/Install_Chrome_OS-1.jpg|Install Chrome OS]]

7. Now, **remove the USB flash drive** and then turn on your Windows PC. This time, your PC will boot straight into full-fledged Chrome OS. In case, Chrome OS is not installed on your PC hard disk and has, in fact, installed on the USB drive then follow our troubleshooting guide below.

_**Note:** Before logging into your Google account, keep in mind, you are officially not allowed to run Chrome OS with Play Store support on non-certified machines. In some ways or the other, you might be violating Google’s terms and conditions. So, I would recommend you to sign in with a secondary Google account so that your primary account remains safe._

![[03 MEDIA & FILES/Install_Chrome_OS_on_PC_with_Play_Store_Support.jpg|Install Chrome OS on PC with Play Store Support]]

8. Now, you can run Android apps straight from the Play Store on your PC, how awesome is that? Not to mention, **the Android framework is based on Android 9** so you are quite updated too.

_**Note:** If you are having issues with WiFi, Bluetooth, or any other hardware device on Chrome OS then go through the Troubleshooting section for help._

![[03 MEDIA & FILES/Install_Chrome_OS-1.jpg|Install Chrome OS]]

9. Apart from that, you can also [set up Linux](https://beebom.com/how-use-linux-chromebook/) on your Windows-turned-Chrome OS machine. You can find the [best Linux apps for Chrome OS](https://beebom.com/best-linux-apps-chromebook/) from the linked article.

![[03 MEDIA & FILES/linux_apps_Install_Chrome_OS_on_PC_with_Play_Store_Support.jpg|linux apps Install Chrome OS on PC with Play Store Support]]

### Troubleshooting Chrome OS on PC

If Chrome OS got **installed on the wrong device i.e. on the USB stick** then follow this simple tutorial to resolve the issue. Generally, the hard disk is named as `sda`, but on some older computers, it is named as `mmcblk0` or something else. And because of this ambiguity, Chrome OS gets installed on the wrong device. So to fix the problem, here is what you need to do.

![[Updated February 2021|[Updated February 2021|[Updated February 2021|[Updated February 2021)](03 MEDIA & FILES/Install_Chrome_OS_on_PC_with_Play_Store_Support_(Updated_February_2021|Install Chrome OS on PC with Play Store Support (Updated February 2021|[Updated February 2021|[Updated February 2021|[Updated February 2021)]]]]]]-1.jpg)

Open the GParted application on Linux Mint (from the start menu) and check the name of your hard disk drive (on the top-right corner). It should be `sda`. If it’s something else then note it down and open install.sh file **using Vim editor on Linux Mint** (just search in the start menu). Replace `sda` with the actual hard disk name in the last line.

![[Updated February 2021|[Updated February 2021|[Updated February 2021|[Updated February 2021)](03 MEDIA & FILES/Install_Chrome_OS_on_PC_with_Play_Store_Support_(Updated_February_2021|Install Chrome OS on PC with Play Store Support (Updated February 2021|[Updated February 2021|[Updated February 2021|[Updated February 2021)]]]]]]-2.jpg)

For example, if the hard disk name is `mmcblk0` then `/dev/sda` in the last line should change to `/dev/mmcblk0`. Now, save the file and execute the install.sh file and it should install Chrome OS on your hard disk. In case, you are unable to edit the install.sh file on Linux Mint, go back to Windows and **download Notepad++** ([Free](https://notepad-plus-plus.org/downloads/)). From there, you can edit the file easily. Make sure to open “Edit” from the menu bar and then choose “EOL Conversion”. After that, choose “Unix” and save the file. Now, execute “install.sh” in Linux Mint and you will have no issues.

![[Updated February 2021|[Updated February 2021|[Updated February 2021|[Updated February 2021)](03 MEDIA & FILES/Install_Chrome_OS_on_PC_with_Play_Store_Support_(Updated_February_2021|Install Chrome OS on PC with Play Store Support (Updated February 2021|[Updated February 2021|[Updated February 2021|[Updated February 2021)]]]]]]-3.jpg)

In case, you are getting an entirely new error like **``syntax error near unexpected token `$’\r’ ‘``** while running the script then open the `chromeos-install.sh` file using Notepad++ on Windows 10. `chromeos-install.sh` file will be available under the “Chrome OS” folder that you moved to the USB drive. After that, follow the same steps as above and change the formatting option to Unix on Notepad++. Open Edit -> EOL Conversion -> Unix and save the file. Now, go ahead with the installation.

If you are **having issues with WiFi, Bluetooth, touchscreen display, etc**. then you can try adding support for your specific hardware device from the Crosh terminal. Just open Chrome and press Ctrl + Alt + T to open the Crosh terminal. After that, enter `shell` and hit enter. Now, run `sudo edit-grub-config`. Here you can add support for your hardware device. You can find the complete list of commands from [[https://github.com/sebanc/brunch/blob/master/README.md#framework-options]].

![[03 MEDIA & FILES/crosh_terminal.jpg|crosh terminal]]

For example, if you have an RT3290/RT3298LE Bluetooth device then you can add “options=rtbth” (**with quotes**) at the end of “cros_debug” and before loop.max…. Now, press Ctrl + X and press “Y”. Next, hit enter to save the file. Finally, restart your computer, and this time Bluetooth should work fine.

Similarly, if you want to **fix WiFi** then first you need to find out the manufacturer of the wireless card. If it’s Broadcom then add to the same line like this: “options=rtbth,broadcom_wl”. This will fix both Bluetooth and WiFi issues. You can remove `rtbth` if Bluetooth is already working for you. Similarly, if it’s Realtek then add “options=rtbth,rtl8188eu” or “options=rtbth,rtl8821ce”. Basically, you can add support for hardware devices in this fashion: “options=option1,option2,…” (without spaces) to activate them.

### Install Chrome OS Flex

If the reason you’re thinking of installing Chrome OS on your Windows 11 PC is that your laptop is getting bogged down with age, you should definitely take a look at Chrome OS Flex. We have a dedicated guide on [how to install Chrome OS Flex on Windows PC](https://beebom.com/how-install-chrome-os-flex-windows-laptop-macbook/) that you can follow to get Chrome OS running on any laptop out there.

## Install Chrome OS on PC in 2022 and Enjoy Android and Linux Apps

So that is how you can install Chrome OS on PC and get all the perks including Google Play Store and Linux support. I tested Chrome OS on my decently-specced Windows laptop (Intel i5) and it was simply flying without any hiccup. The performance difference was amazing, to say the least. To learn more about the advantage of [Chromebooks over Windows laptops](https://beebom.com/chromebook-vs-laptop/), you can go through our in-depth article.

And in case, you have made your mind to stick with Chrome OS then make sure to take advantage of Linux apps. It’s pretty good and works like a charm. Also, if you miss Windows apps then you can use Wine to [run Windows apps on Chrome OS](https://beebom.com/how-use-windows-10-apps-chromebook-using-wine/). Anyway, that is all from us. If you are facing any problem while installing Chrome OS on your PC then comment down below and let us know. We will surely try to help you out.