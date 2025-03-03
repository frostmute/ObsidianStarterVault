---
created: 2024-06-29
source: https://forums.kali.org/
category:
  - "[[../00 - CATEGORIES/Clippings]]"
cssclasses:
  - obsidian-banner
poster: "![[.md|poster]]"
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
url: https://forums.kali.org/
title: "driver rtl8812bu"
description: "I've been trying for a week to figure out how to install rtl8812bu ... none of the instructions or description works ..... when I give "lsusb" ..... I write that the device sees but in the wifi overview connected at the top right corner nothing ... ..just an old card that is fixed in the laptop"
host: forums.kali.org
image: 
```
1.  > I've been trying for a week to figure out how to install rtl8812bu ... none of the instructions or description works ..... when I give "lsusb" ..... I write that the device sees but in the wifi overview connected at the top right corner nothing ... ..just an old card that is fixed in the laptop
    
2.  > I have been troubleshooting no injection on certain kernels to internal wifi not on, so I learned A few things. Did you download the driver from git? And what version. Rtl8812bu is easier to install than au. Anyway google rtl8812bu fastoe git. Try that driver, read the read me. mv download rtl8812bu to /usr/src/ , cd to /usr/src/rtl8812bu ,run all commands in this directory.
    
3.  > I have found a solution to this issue that works for my AC1200 dual band card, with packet injection support and monitor mode working. I would strongly suggest you check your chipset and make sure that it is compatible (mine is a BrosTrend AC1200 dual band V2 card) before attempting this. I used [this](https://github.com/cilynx/rtl88x2bu) driver from cilynx on GH. I clone the repository and built the driver from source. The precompiled debian packages never fully installed a gave me a dkms error when adding the module to the kernel headers. After building from source, I restarted and left the card plugged into my laptop, and it was recognized by Kali with full support like an Alfa card.
    > 
    > To build the driver from source is not a scary task. First you'll need to make sure you have the dependencies installed before you build. Then you'll have to locate your source code folder, build your driver and install it. Open a terminal and type:
    > 
    > sudo apt-get install build-essential build-dep
    > 
    > cd /your/source-code/folder
    > 
    > make
    > 
    > sudo make installAfter this, your driver should be installed and to ensure proper function, I suggest restarting and leaving the wifi adapter plugged in on reboot so that it is recognized and configured correctly.
    
    > ***Time is precious. Waste it wisely.***
    > 
    > ***Just because something is illegal, doesn't make it wrong.***
    > 
    > ***Just because something is legal, doesn't make it right.***
> rtl8812bu,driver,sees,wifi,overview,connected,corner,card,fixed,device,give,write,week,figure,lsusb,install,instructions,description,works,laptop