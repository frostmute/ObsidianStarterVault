---
created: 2024-06-29
source: https://www.quora.com/How-do-I-check-if-my-wireless-adapter-supports-monitoring-mode
category:
  - "[[../00 - CATEGORIES/Clippings]]"
cssclasses:
  - obsidian-banner
poster: "![poster](../03%20-%20MEDIA%20&%20FILES/50f6d8ecfb0675891ef0eb41c01f6ba9_MD5.webp)"
feature: "![[../03 - MEDIA & FILES/50f6d8ecfb0675891ef0eb41c01f6ba9_MD5.webp]]"
---

![banner](../03%20-%20MEDIA%20&%20FILES/50f6d8ecfb0675891ef0eb41c01f6ba9_MD5.webp)

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
url: https://www.quora.com/How-do-I-check-if-my-wireless-adapter-supports-monitoring-mode
title: "How do I check if my wireless adapter supports monitoring mode? - Quora"
description: 
host: www.quora.com
image: https://qsf.cf2.quoracdn.net/-4-images.Illustration_fb_share_default_1280x720.png-26-7b8bc71e8107b6f5.png
```
Others, happy reading : )

The manufacturers have hard coded it to not to perform any kind of monitoring Or package injection in it.. But there is a guy who found out to overwrite the kernel to our advantage!! Believe me!! It does work for me!!! Earlier..i couldn't even change my MAC address. Now I can!! Thanks to this guy..kimocoder..

Before I explain how I did it…

Have you ever tried this..



When you check the mode, you will still get this..


Well.. Then.. How to convert it to monitor mode and run those juicy aireplay-ng commands??

Here it is…

-   STEP 1

MAKE SURE THAT YOU ARE ALWAYS IN ROOT!

Clone this url from github…



-   STEP 2

Blacklist the previous driver..



-   STEP 3

Change your directory into the downloaded directory from GitHub.

I assume you can do this.. If you can't then I would suggest you to take a course on basic linux commands first.

-   STEP 4

perform the compilation by typing in the command..



-   STEP 5

Install the compilation



Once again I am reminding you.. ALL THE TIME, YOU GOTTA BE IN ROOT!!

-   STEP 6

Reboot your system



-   STEP 7

Perform this to enable the monitor mode..

Firstly, we have to kill the processes that may interfere with monitoring.



Then.. Normally we would type in airmon-ng start wlan0 or iwconfig wlan0 set mode monitor right?? But trust me!! It won't work here.. The only command that will work is…



And BOOM!!!

WE ARE IN MONITOR MODE… TRY CHECKING IT BY TYPING IN iwconfig

Some NOTES TO TAKE…

1.  The monitoring will be conducted on wlan0. No new name will be assigned to you like wlan0mon or mon0 etc.
2.  Every time you want to switch to monitor mode try using the iw dev… command rather than the iwconfig wlan0 set… command.

That's it folks.. Now enjoying cracking, sniffing, deauthenticating, creating fake access points on the network.

See ya guys later!

Signing off

MASK.
> 