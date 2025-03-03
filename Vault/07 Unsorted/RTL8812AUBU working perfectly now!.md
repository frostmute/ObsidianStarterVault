---
created: 2024-06-29
source: https://forum.aircrack-ng.org/index.php?topic=8129.0
category:
  - "[[Clippings]]"
cssclasses:
  - obsidian-banner
poster: "![poster]()"
feature: "![[../03 - MEDIA & FILES/4d326c1c65db3f5054b7849a762fd01b_MD5.gif]]"
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
url: https://forum.aircrack-ng.org/index.php?topic=8129.0
title: "RTL8812AU/BU working perfectly now!"
description: "RTL8812AU/BU working perfectly now!"
host: forum.aircrack-ng.org
image: 
```
Sorry Guest, you are banned from posting and sending personal messages on this forum.

This ban is not set to expire.

### ![](../03%20-%20MEDIA%20&%20FILES/4d326c1c65db3f5054b7849a762fd01b_MD5.gif) Author Topic: RTL8812AU/BU working perfectly now!  (Read 15375 times)

***

A quick run down, I have had this USB adapter for over two months and at one point in time, I had it working. I ran "dist-upgrade" after an update and that was the beginning of the end. After two OS changes (Parrot and Kali) and another Usb adapter Rtl8812BU I am finally back to that point. I have both USB wifis up and working. Monitor mode, injection and captured handshakes , best I have ever seen. Fluxion is a killer for handshakes and Bettercap 2.0 very good at more in-depth "pentesting". Wireshark tls eapol filter works after much playing around with. Anyway this is what I am working with. HP zbook...Linux kernel  v5.4.0-66-generic...Ubuntu 20.04.2 LTS...RTL8812AU/21AU v5.6.4.2 and RTL88x2BU v5.6.1.  One issue I have is Ubuntu 20.04 come with dkms for RTL8812AU in repo v4.3.8 and it is also installed. I do not want to remove other driver (5.6.1) so if it ain't broke, don't fix it.

![](../03%20-%20MEDIA%20&%20FILES/8ac61eb352fd349833969bf3dab7c383_MD5.gif) Logged

***

P.S. I did compile aircrack-ng from source to get latest version. ![;)](../03%20-%20MEDIA%20&%20FILES/3e2d9b0dd8c11107529857e9be7fad5a_MD5.gif "Wink")

![](../03%20-%20MEDIA%20&%20FILES/8ac61eb352fd349833969bf3dab7c383_MD5.gif) Logged

***

PS  
Do not upgrade to kernel v5.10.0  Injection will stop working on rtl8812au.

![](../03%20-%20MEDIA%20&%20FILES/8ac61eb352fd349833969bf3dab7c383_MD5.gif) Logged

***

> A quick run down, I have had this USB adapter for over two months and at one point in time, I had it working. I ran "dist-upgrade" after an update and that was the beginning of the end. After two OS changes (Parrot and Kali) and another Usb adapter Rtl8812BU I am finally back to that point. I have both USB wifis up and working. Monitor mode, injection and captured handshakes , best I have ever seen. Fluxion is a killer for handshakes and Bettercap 2.0 very good at more in-depth "pentesting". Wireshark tls eapol filter works after much playing around with. Anyway this is what I am working with. HP zbook...Linux kernel  v5.4.0-66-generic...Ubuntu 20.04.2 LTS...RTL8812AU/21AU v5.6.4.2 and RTL88x2BU v5.6.1.  One issue I have is Ubuntu 20.04 come with dkms for RTL8812AU in repo v4.3.8 and it is also installed. I do not want to remove other driver (5.6.1) so if it ain't broke, don't fix it.  

Realtek USB wifi will not work on kernel v5.10.0, if you upgrade,injection will not work. Mediatek  mt7610u is stated to work with the latest kernel. I have ordered one but until it arrives I can not verify this.

![](../03%20-%20MEDIA%20&%20FILES/8ac61eb352fd349833969bf3dab7c383_MD5.gif) Logged
> 