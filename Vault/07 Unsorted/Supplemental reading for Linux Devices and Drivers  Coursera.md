---
banner: https://s3.amazonaws.com/coursera/media/Grid_Coursera_Partners_updated.png
created: 2024-06-17T10:51:43
source: https://www.coursera.org/learn/os-power-user/supplement/Smg89/supplemental-reading-for-windows-software-packages
author: 
cssclasses: []
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

```cardlink
url: https://www.coursera.org/learn/os-power-user/supplement/Smg89/supplemental-reading-for-windows-software-packages
title: "Supplemental reading for Linux Devices and Drivers | Coursera"
description: "In the third module of this course, we'll learn about package and software management in Windows and Linux OS. It's important to know how package installs work and how devices and drivers are managed within these operating systems. We will also ..."
host: www.coursera.org
image: https://s3.amazonaws.com/coursera/media/Grid_Coursera_Partners_updated.png
```
# Supplemental reading for Linux Devices and Drivers

## Linux Devices and Drivers

In this reading, you will learn how devices and drivers are managed in Linux. Previously, you learned that in Linux, devices attached to the computer are recognized by the operating system as device files. Devices are located in the /dev directory in Linux. A few examples of devices you may find in the /dev directory include:

-   **/dev/sda** \- First SCSI drive
    
-   **/dev/sr0** - First optical disk drive 
    
-   **/dev/usb** - USB device
    
-   **/dev/usbhid** - USB mouse
    
-   **/dev/usb/lp0** - USB printer
    
-   **/dev/null** - discard
    

Some of the Linux device categories include:

-   **Block devices:** Devices that can hold data, such as hard drives, USB drives, and filesystems.
    
-   **Character devices:** Devices that input or output data one character at a time, such as keyboards, monitors, and printers. 
    
-   **Pipe devices:** Similar to character devices. However, pipe devices send output to a process running on the Linux machine instead of a monitor or printer.
    
-   **Socket devices:** Similar to pipe devices. However, socket devices help multiple processes communicate with each other.
    

### Installing a device in Linux

There are hundreds of versions of Linux available due to the fact that Linux is an open source operating system. The methods for installing devices on Linux can vary from version to version. The instructions in this section provide various options for installing a printer and its device drivers on a Red Hat 9 Linux system running the GNOME user interface.

**Device autodetect with udev**

Udev is a device manager that automatically creates and removes device files in Linux when the associated devices are connected and disconnected. Udev has a daemon running in Linux that listens for kernel messages about devices connecting and disconnecting to the machine.

**Installation through a user interface - GNOME**

There are multiple user interfaces available for Linux. These instructions are specifically for the GNOME user interface. 

1.  In the GNOME user interface, open the **Settings** menu.
    
2.  On the left-side menu, select **Printers**.
    
3.  Click the **Unlock** button in the top right corner to change the system settings. Note that your user account must have *superuser*, *sudo,* or *printadmin* privileges to unlock the system settings for printers. 
    
4.  A dialog box will open showing a list of available printers. If your network has a large number of printers, you can search for the printer by IP address or host name. 
    
5.  Select the printer you want to install on the local system and click **Add**.
    
6.  The printer listing will appear in the **Settings** window for the **Printers.** 
    
7.  In the top right corner of the printer listing, click the **Printer Settings** icon and select **Printer Details** from the pop-up menu. 
    
8.  The details of the printer will open in a new window. You should have three options for installing the printer driver:
    
    1.  **Search for Drivers:** The GNOME Control Center will automatically search for the driver in driver repositories using PackageKit.
        
    2.  **Select from Database:** Manually select a driver from any databases installed on the Linux system.
        
    3.  **Install PPD File:** Manually select from a list of postscript printer description (PPD) files, which may be used as printer drivers.
        

**Installation through the command line**

Red Hat Linux uses the Common Unix Printing System (CUPS) to manage printers from the command line. CUPS servers broadcast to clients for automatic printer installation on Linux machines. However, for network environments with multiple printers, it may be preferable to manually install specific printers through the command line. 

-   From the command-line, enter **$ lpadmin -p** **printername -m driverfilename.ppd** 
    
    -   **Lpadmin** is the printer administrator command.
        
    -   The **\-p printername** command adds or modifies the named printer. 
        
    -   The **\-m driverfilename.ppd** command installs the postscript printer description (PPD) driver filename that you provide. The file should be stored in the **/usr/share/cups/model/** directory.
        
    -   Enter **$ man lpadmin** to open the manual for the lpadmin command to find additional command line options.
        

### How to check if a device is installed

There are a couple of methods for checking if a device is already installed on a Linux machine:

**Through a user interface like GNOME**

1.  In the GNOME user interface, open the **Settings** menu.
    
2.  Browse each device set on the left-side menu. 
    
3.  The attached devices of the selected device type will appear in the window pane on the right.
    

**Through the command line**

Here are some commands that list specific device types: 

-   **$ ls /dev** - Lists all devices in the /dev folder 
    
-   **$ lcpci** \- Lists devices installed on the PCI bus 
    
-   **$ lsusb** \- Lists devices installed on the USB bus
    
-   **$ lsscsi** \- Lists SCSI devices, such as hard drives
    
-   **$ lpstat -p** \- Lists all printers and whether they are enabled
    
-   **$ dmesg** - Lists devices recognized by the kernel
> 