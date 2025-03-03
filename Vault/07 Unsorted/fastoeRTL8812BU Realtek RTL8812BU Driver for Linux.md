---
created: 2024-06-29
source: https://github.com/fastoe/RTL8812BU
category:
  - "[[../00 - CATEGORIES/Clippings]]"
cssclasses:
  - obsidian-banner
poster: "![poster](https://opengraph.githubassets.com/67a1e6e39301ae387d4442de8de6689a86ca822165fde832b63c7d3714cef9e7/fastoe/RTL8812BU)"
feature: "![[../03 - MEDIA & FILES/6b1c0a2ca47318181b0ef02e07caa4a6_MD5.png]]"
---

![banner](../03%20-%20MEDIA%20&%20FILES/6b1c0a2ca47318181b0ef02e07caa4a6_MD5.png)

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
url: https://github.com/fastoe/RTL8812BU
title: "fastoe/RTL8812BU: Realtek RTL8812BU Driver for Linux"
description: "Realtek RTL8812BU Driver for Linux. Contribute to fastoe/RTL8812BU development by creating an account on GitHub."
host: github.com
image: https://opengraph.githubassets.com/67a1e6e39301ae387d4442de8de6689a86ca822165fde832b63c7d3714cef9e7/fastoe/RTL8812BU
```
## Realtek RTL8812BU Driver for Linux

[![Build Status](https://github.com/fastoe/RTL8812BU/actions/workflows/rtl8812bu.yml/badge.svg)](https://github.com/fastoe/RTL8812BU/actions)

Driver for 802.11ac USB adapter with RTL8812BU chipset, only STA/Monitor mode is supported, no AP mode.

A few known wireless cards that use this driver include:

-   [Fastoe AC1200 USB Wi-Fi Adapter](https://www.amazon.com/1200Mbps-ChromeBook-802-11ac-Compatible-Raspbian/dp/B081TGWCVB/ref=as_li_ss_tl?m=A9879GOT1YWJ2&marketplaceID=ATVPDKIKX0DER&qid=1581225299&s=merchant-items&sr=1-3&linkCode=ll1&tag=fastoe-20&linkId=5648949a51280f0323dd599dc27dbae4&language=en_US)
-   Cudy WU1200 AC1200 High Gain USB Wi-Fi Adapter
-   TP-Link Archer T3U
-   TP-Link Archer T3U Plus
-   TP-Link Archer T4U V3
-   Linksys WUSB6400M
-   Dlink DWA-181
-   Dlink DWA-182

Currently tested with Linux kernel 4.12.14/4.15.0/5.3.0/5.15.0 on X86\_64 platform **only**.

### For Raspberry Pi

-   [https://github.com/fastoe/RTL8812BU\_for\_Raspbian](https://github.com/fastoe/RTL8812BU_for_Raspbian)

### For kernel 5.11 or later, please clone the v5.13.1 branch:

```shell
sudo apt update
sudo apt install -y build-essential dkms git bc
git clone -b v5.13.1 https://github.com/fastoe/RTL8812BU.git
cd RTL8812BU
make
sudo make install
sudo reboot
```

### For 5.10 kernel, please clone the v5.6.1 branch:

```shell
sudo apt update
sudo apt install -y build-essential dkms git bc
git clone -b v5.6.1 https://github.com/fastoe/RTL8812BU.git
cd RTL8812BU
make
sudo make install
sudo reboot
```

### For 5.9 and previous versions:

```shell
sudo apt update
sudo apt install -y build-essential dkms git bc
git clone https://github.com/fastoe/RTL8812BU.git
cd RTL8812BU
make
sudo make install
sudo reboot
```

For setting monitor mode:

```shell
# configure for monitor mode
sed -i 's/CONFIG_80211W = n/CONFIG_80211W = y/' Makefile
sed -i 's/CONFIG_WIFI_MONITOR = n/CONFIG_WIFI_MONITOR = y/' Makefile

make
sudo make install
sudo ip link set wlx1cbfcea97791 down
sudo iw wlx1cbfcea97791 set monitor none
sudo ip link set wlx1cbfcea97791 up
```

[![image](https://camo.githubusercontent.com/a5157ce4dcd4c58774fbb59ca1b337db37299e27feda4a78b9483c071ff8a0a7/68747470733a2f2f7777772e666173746f652e636f6d2f696d616765732f323032302f30352f3838313262752d6d6f6e69746f722d6d6f64652e706e67)](https://camo.githubusercontent.com/a5157ce4dcd4c58774fbb59ca1b337db37299e27feda4a78b9483c071ff8a0a7/68747470733a2f2f7777772e666173746f652e636f6d2f696d616765732f323032302f30352f3838313262752d6d6f6e69746f722d6d6f64652e706e67)

Enjoy!
> 