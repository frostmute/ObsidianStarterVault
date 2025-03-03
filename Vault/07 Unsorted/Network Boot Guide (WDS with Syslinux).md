---
created: 2024-07-04
source: https://www.d7xtech.com/tech-info/network-boot-guide/
category:
  - "[[Clippings]]"
cssclasses:
  - obsidian-banner
  - page-grid
  - pen-white
  - dashboard
poster: "![poster](../03%20-%20MEDIA%20&%20FILES/Pasted%20image%2020240704154005.png)"
tags:
  - clippings
  - technical
  - ItSupport
  - linux
feature: "![[../03 - MEDIA & FILES/Pasted image 20240704154005.png]]"
---

![banner](../03%20-%20MEDIA%20&%20FILES/Pasted%20image%2020240704154005.png)


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

```meta-bind-button
label: Un-Fold All
icon: ""
hidden: false
class: ""
tooltip: ""
id: "002"
style: primary
actions:
  - type: command
    command: editor:unfold-all
```

***

```cardlink
url: https://www.d7xtech.com/tech-info/network-boot-guide/
title: "Network Boot Guide (WDS with Syslinux) – d7xTech.com (formerly Foolish IT)"
description: "Network Boot Guide Update:  People keep asking about booting to UEFI, and I had someone figure out something and I think I have a solution.  See the Install Syslinux section for new info on that. A…"
host: www.d7xtech.com
image: 
```

***
### **Network Boot Guide**

**Update:**  People keep asking about booting to UEFI, and I had someone figure out something and I think I have a solution.  See the Install Syslinux section for new info on that.

A tech’s guide on creating a server running **WDS (Windows Deployment Services) integrated with Syslinux**.  This allows you to boot to the network for Windows image deployments (complete with Windows updates, specific drivers, and even your favorite apps to pre-load on a clean install) as well as your favorite tech tools with their own boot environments (such as [Memtest86+](http://www.memtest.org/)) including many Linux boot or ‘Live’ CDs!

***Requirements:***  A spare Windows server license capable of Windows Deployment Services, and the hardware to run it on *(or a very capable virtual machine!)*  Windows Server 2008 R2 was used in creating this guide.

***Note:***  Windows XP, Vista, and 7 are specifically referenced for image deployments in the guide, but Windows 10 should also work with the same process.

***Note:***  The following article originally titled “My Network Boot Setup” was originally published sometime in 2012, and it has not been updated since that time.  With that in mind, please prepare yourself if some information *(especially with Syslinux)* may be dated to the point of needing modification.  If you notice anything wrong and do figure out the updated process/steps, [please let us know](https://www.d7xtech.com/contact-us)!

#### **“My Network Boot Setup”**

It seems there are a lot of techs still doing things the hard way:  fumbling around with dozens of CDs for various tasks (e.g. boot CDs, Windows install CDs, etc.)  *Why?*  Most modern PCs *(and a lot of very old ones)* allow for a PXE network boot option, which can be a huge advantage in your tech shop to cover these tasks *(with the right server setup!)*

***Update:***  These days there are also utilities you can use on a flash drive or USB hard drive, boot CD, or even a floppy disk to boot to the network on systems without PXE capabilities or without having to enable that in the BIOS…  See [Yumi](http://www.pendrivelinux.com/yumi-multiboot-usb-creator/) or …

In this guide we explain how you can take advantage of this to *(mostly)* rid yourself of your growing CD collection and learn to deploy a fresh install of Windows XP-7 in mere minutes, including current Windows updates, drivers, and any apps you would like to have pre-installed!  Using a combination of WDS (Windows Deployment Services) with Syslinux, you can streamline your workflow with very simple processes while saving time and money!

***Note:***  A bit of credit must go towards [this other guy’s blog](http://thommck.wordpress.com/2011/09/09/deep-dive-combining-windows-deployment-services-pxelinux-for-the-ultimate-network-boot/) for the integration of Syslinux with WDS, though the instructions weren’t as complete as I would have liked them to be (memdisk among other things weren’t included.)

#### **Getting Started**

To get started quickly with minimal configuration, start by reviewing the [**Install WDS**](https://www.d7xtech.com/tech-info/network-boot-guide/install-wds/) and [**Install Syslinux**](https://www.d7xtech.com/tech-info/network-boot-guide/install-syslinux/) sections **first**, then once you are up and running you can venture off into the subsections listed in the Network Boot Guide below.

***

#### **Network Boot Guide**    <- You are here!

-   [**Install WDS**](https://www.d7xtech.com/tech-info/network-boot-guide/install-wds/) (Windows Deployment Services)
    -   [Add Vista/7 Images to WDS](https://www.d7xtech.com/tech-info/network-boot-guide/install-wds/add-vista-7-images/)
    -   [Add Drivers to boot.wim (for Vista/7 Images)](https://www.d7xtech.com/tech-info/network-boot-guide/install-wds/add-drivers-to-boot-wim/)
    -   [Add Drivers to XP Images (with Sysprep.inf)](https://www.d7xtech.com/tech-info/network-boot-guide/install-wds/add-drivers-to-xp-images-sysprep-inf/)
    -   [Add XP or Modified Vista/7 Images to WDS](https://www.d7xtech.com/tech-info/network-boot-guide/install-wds/add-xp-or-modified-vista-7-images/)
-   [**Install Syslinux**](https://www.d7xtech.com/tech-info/network-boot-guide/install-syslinux-on-wds/)
    -   [Add Boot Images to Syslinux on WDS](https://www.d7xtech.com/tech-info/network-boot-guide/install-syslinux-on-wds/add-boot-images/)
-   **[Troubleshooting Issues](https://www.d7xtech.com/tech-info/network-boot-guide/troubleshooting-issues/)**
> 