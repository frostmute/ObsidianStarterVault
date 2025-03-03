---
created: 2024-06-29
source: https://deviwiki.com/wiki/ASUS_USB-AC53_Nano
category:
  - "[[../00 - CATEGORIES/Clippings]]"
cssclasses:
  - obsidian-banner
feature: "![[../03 - MEDIA & FILES/1f54dbb7873af6708d476144adb4f17d_MD5.png]]"
---

![banner](../03%20-%20MEDIA%20&%20FILES/1f54dbb7873af6708d476144adb4f17d_MD5.png)

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
url: https://deviwiki.com/wiki/ASUS_USB-AC53_Nano
title: "ASUS USB-AC53 Nano - DeviWiki (ex WikiDevi)"
description: "ASUS USB-AC53 Nano"
host: deviwiki.com
image: https://deviwiki.com/w/resources/assets/mediawiki.png
```

**ASUS** USB-AC53 **Nano**

**<small>Manuf/OEM/ODM</small>** **Edimax** EW-7822UNC

**FCC approval date:** 29 December 2016  

**Amazon image**  
[](https://www.amazon.com/dp/B071KV2SMV?tag=wiki086-20)  
**ASIN**  
B071KV2SMV <small>(<span title="United States"><img alt="Flag of the United States.svg" src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/a4/Flag_of_the_United_States.svg/13px-Flag_of_the_United_States.svg.png" decoding="async" width="13" height="7" srcset="https://upload.wikimedia.org/wikipedia/commons/thumb/a/a4/Flag_of_the_United_States.svg/20px-Flag_of_the_United_States.svg.png 1.5x, https://upload.wikimedia.org/wikipedia/commons/thumb/a/a4/Flag_of_the_United_States.svg/26px-Flag_of_the_United_States.svg.png 2x"></span>, <a rel="nofollow" href="https://www.amazon.com/dp/B071KV2SMV?tag=wiki086-20">On <b>Amazon</b></a>, <a rel="nofollow" href="http://camelcamelcamel.com/product/B071KV2SMV">On <b>CCC</b></a>)</small>  
**<small><span color="red">multiple revisions of this device, use caution</span></small>**  
**[On Newegg](https://www.newegg.com/Product/Product.aspx?Item=0XM-005U-00042)**

**Interface: USB**

**USB 2.0**  
**Connector:** Male A  
**Form factor tags:** nano dongle

**ID:** [0b05:184c](http://usb-ids.gowdy.us/read/UD/0b05/184c)  
<small>Windows: <b>USB\VID_0B05&amp;PID_184C</b></small>

**WI1 chip1:** **Realtek** RTL8812BU

**Antenna connector:** **none**

**abgn+ac, 2x2:2**

**Flags:** MU-MIMO

<small>For a list of all currently documented <b>Realtek</b> chipsets with specifications, see <b><a href="https://deviwiki.com/wiki/Realtek" title="Realtek">Realtek</a></b>.</small>  

***

_**Dual-band Wireless-AC1200 USB Adapter**_

[Product page](http://www.asus.com/Networking/USB-AC53-Nano)  • [Support page](https://www.asus.com/Networking/USB-AC53-Nano/HelpDesk/)  • [Downloads](https://www.asus.com/Networking/USB-AC53-Nano/HelpDesk_Download/)

- "EW-7822UNC" and "P/C=F119-223" is silkscreened on the board (top).
- "1246-00000172-50Z" and "1637" is silkscreened on the board (bottom).

A thernal pad is attached to the RTL8812BU IC to conduct heat into the USB connector.

### Linux Support

- [*Driver for Asus USB-AC53 Nano* on **UbuntuForums**](https://ubuntuforums.org/showthread.php?t=2362577)
- [*Driver for Asus USB-AC53 Nano* on **UbuntuForums**](https://ubuntuforums.org/showthread.php?t=2362669)

Driver **rtl8822bu** on [Edimax EW-7822ULC](https://deviwiki.com/wiki/Edimax_EW-7822ULC "Edimax EW-7822ULC"): [*Download*](http://www.edimax.com/edimax/mw/cufiles/files/download/Driver_Utility/EW-7822ULC_Linux_Driver_1.0.0.9.zip)

```
<small> Bus 001 Device 003: ID 0b05:184c ASUSTek Computer, Inc.
 usb 1-1.2: new high-speed USB device number 4 using dwc_otg
 usb 1-1.2: New USB device found, idVendor=0b05, idProduct=184c
 usb 1-1.2: New USB device strings: Mfr=1, Product=2, SerialNumber=3
 usb 1-1.2: Product: 802.11ac NIC
 usb 1-1.2: Manufacturer: Realtek
 usb 1-1.2: SerialNumber: 123456
</small>
```

- [**jeremyb31/rtl8822bu**](https://github.com/jeremyb31/rtl8822bu/blob/2bca1c86ac0aded009a0d9307abe0afd622f7c69/os_dep/linux/usb_intf.c) ([commit](https://github.com/jeremyb31/rtl8822bu/commit/2bca1c86ac0aded009a0d9307abe0afd622f7c69))

For linux kernel version > 4.14 jeremyb31's driver will not work so far,

but with the changes from [**y0urself/rtl8822bu**](https://github.com/y0urself/rtl8822bu) you will be fine!

- [**MeissnerEffect/rtl8822bu**](https://github.com/MeissnerEffect/rtl8822bu)

For linux kernel version > 4.15 (init\_timer deprecation) check.

## Images

- [![](../03%20-%20MEDIA%20&%20FILES/fa0d6b3c81b38183f9e737431453b7c9_MD5.jpg)](https://deviwiki.com/wiki/File:ASUS_USB-AC53_Nano_board_top.jpg)
		
		board top
		
- [![](../03%20-%20MEDIA%20&%20FILES/d001d338606b72d5a09bc8563dbdcaca_MD5.jpg)](https://deviwiki.com/wiki/File:ASUS_USB-AC53_Nano_board_bot.jpg)
		
		board bottom
		

## See also

[Asus Wireless Adapters Products](http://www.asus.com/Networking/Wireless-Adapters-Products/)

- [ASUS USB-AC68](https://deviwiki.com/wiki/ASUS_USB-AC68 "ASUS USB-AC68") - Dual-Band AC1900 USB Wi-Fi Adapter
- [ASUS USB-AC56](https://deviwiki.com/wiki/ASUS_USB-AC56 "ASUS USB-AC56") - Dual-Band AC1300 USB 3.0 Wi-Fi Adapter
- [ASUS USB-AC56R](https://deviwiki.com/wiki/ASUS_USB-AC56R "ASUS USB-AC56R") - Dual-Band AC1300 USB 3.0 Wi-Fi Adapter
- [ASUS USB-AC55 B1](https://deviwiki.com/wiki/ASUS_USB-AC55_B1 "ASUS USB-AC55 B1") - Dual-Band AC1300 USB 3.0 Wi-Fi Adapter
- [ASUS USB-AC55](https://deviwiki.com/wiki/ASUS_USB-AC55 "ASUS USB-AC55") - Dual-Band AC1300 USB 3.0 Wi-Fi Adapter
- [ASUS USB-AC54](https://deviwiki.com/wiki/ASUS_USB-AC54 "ASUS USB-AC54") - Dual-Band AC1300 USB 3.0 Wi-Fi Adapter
- [ASUS USB-AC53](https://deviwiki.com/wiki/ASUS_USB-AC53 "ASUS USB-AC53") - Dual-Band AC1200 USB Wi-Fi Adapter
- [ASUS USB-AC51](https://deviwiki.com/wiki/ASUS_USB-AC51 "ASUS USB-AC51") - Dual-Band AC600 USB Wi-Fi Adapter
- [ASUS USB-AC50](https://deviwiki.com/wiki/ASUS_USB-AC50 "ASUS USB-AC50") - 5GHz Wireless AC450 USB Wi-Fi Adapter
