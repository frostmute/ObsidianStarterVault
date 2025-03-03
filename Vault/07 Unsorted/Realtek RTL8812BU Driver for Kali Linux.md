---
created: 2024-06-29
source: https://forums.kali.org/
category:
  - "[[Clippings]]"
cssclasses:
  - obsidian-banner
poster: "![poster]()"
feature: "![[https://forums.kali.org/images/buttons/collapse_40b.png]]"
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
url: https://forums.kali.org/
title: "Realtek RTL8812BU Driver for Kali Linux"
description: "Hello all, 
 
Just felt I'd throw this out there as I had this issue so surely someone else will too. 
 
How to get the Realtek RTL8812BU driver installed on Kali (Kernel 4.19.28-2 at time of writing) 
 
From a 100% fresh install, connected to the internet (via NAT Network or whatever), run the following commands: 
 
apt update 
apt install bc -y"
host: forums.kali.org
image: 
```
-   [![Home](https://forums.kali.org/images/misc/navbit-home.png "Home")](https://forums.kali.org/index.php?s=60e92a0902bbff5fd79993d5385640e4)
-   [Forum](https://forums.kali.org/forum.php?s=60e92a0902bbff5fd79993d5385640e4)
-   [Kali Linux Forums](https://forums.kali.org/forumdisplay.php?1-Kali-Linux-Forums&s=60e92a0902bbff5fd79993d5385640e4)
-   [Community Generated How-Tos](https://forums.kali.org/forumdisplay.php?10-Community-Generated-How-Tos&s=60e92a0902bbff5fd79993d5385640e4)
-   [How-To Archive](https://forums.kali.org/forumdisplay.php?31-How-To-Archive&s=60e92a0902bbff5fd79993d5385640e4)
-   Realtek RTL8812BU Driver for Kali Linux

1.  If this is your first visit, be sure to check out the [**FAQ**](https://forums.kali.org/faq.php?s=60e92a0902bbff5fd79993d5385640e4) by clicking the link above. You may have to [**register**](https://forums.kali.org/register.php?s=60e92a0902bbff5fd79993d5385640e4) before you can post: click the register link above to proceed. To start viewing messages, select the forum that you want to visit from the selection below.

1.  ## Realtek RTL8812BU Driver for Kali Linux
    
    > Hello all,
    > 
    > Just felt I'd throw this out there as I had this issue so surely someone else will too.
    > 
    > How to get the Realtek RTL8812**B**U driver installed on Kali (Kernel 4.19.28-2 at time of writing)
    > 
    > From a 100% fresh install, connected to the internet (via NAT Network or whatever), run the following commands:
    > 
    > Code:
    > 
    > ```
    > apt update
    > apt install bc -y
    > git clone https://github.com/cilynx/rtl88x2BU_WiFi_linux_v5.3.1_27678.20180430_COEX20180427-5959.git
    > cd rtl88x2BU_WiFi_linux_v5.3.1_27678.20180430_COEX20180427-5959
    > VER=$(sed -n 's/\PACKAGE_VERSION="\(.*\)"/\1/p' dkms.conf)
    > sudo rsync -rvhP ./ /usr/src/rtl88x2bu-${VER}
    > sudo dkms add -m rtl88x2bu -v ${VER}
    > sudo dkms build -m rtl88x2bu -v ${VER}
    > sudo dkms install -m rtl88x2bu -v ${VER}
    > sudo modprobe 88x2bu
    > ```
    > 
    > After running all that, you should see your 8812BU in ifconfig and you should be able to monitor and packet inject with it.
    > 
    > Note: With time, the author of the driver may make a new major release, so be sure to check for a new repo at [https://github.com/cilynx/](https://github.com/cilynx/)
    > 
    > Cheers guys
    
2.  > How did you test monitor and inject?
    > 
    > In my just full-upgraded Kali VM 64:
    > 
    > Code:
    > 
    > ```
    > root@kali:~# airmon-ng check kill &amp;&amp; airmon-ng start wlan0
    > PHYInterfaceDriverChipset
    > phy1wlan0rtl88x2buRealtek Semiconductor Corp. 802.11ac NIC
    > ERROR adding monitor mode interface: command failed: Operation not supported (-95)
    > ```
    
3.  ## TP-LINK Archer AC1300 T4U V3 Monitor mode
    
    > ![Quote](https://forums.kali.org/images/misc/quote_icon.png "Quote") Originally Posted by **ovosodo** [![View Post](https://forums.kali.org/images/buttons/viewpost-right.png "View Post")](https://forums.kali.org/showthread.php?s=60e92a0902bbff5fd79993d5385640e4&p=86994#post86994)
    > 
    > How did you test monitor and inject?
    > 
    > In my just full-upgraded Kali VM 64:
    > 
    > Code:
    > 
    > ```
    > root@kali:~# airmon-ng check kill &amp;&amp; airmon-ng start wlan0
    > PHY    Interface    Driver        Chipset
    > phy1    wlan0        rtl88x2bu    Realtek Semiconductor Corp. 802.11ac NIC
    > ERROR adding monitor mode interface: command failed: Operation not supported (-95)
    > ```
    > 
    > Hi Guys,
    > 
    > I am running into the exact same issue any suggestions will be highly appreciated.
    
4.  > This driver also work with RTL8812AU. To enable monitor mode. start fluxion "./fluxion.sh" enter option 2 for capturing handshake. After the wifi adapter is initialised. open another terminal tab. Then you can enter "airodump-ng fluxwl0".
    
5.  ## ![Lightbulb](https://forums.kali.org/images/icons/icon3.png "Lightbulb") I hope it will help you with enabling monitor mode.
    
    > I think you can also use this method to enable monitor mode -  
    > Code:  
    > root@kali:~#ifconfig wlan0 down  
    > root@kali:~#airmon-ng check kill  
    > root@kali:~#iwconfig wlan0 mode monitor  
    > root@kali:~#ifconfig wlan0 up  
    > root@kali:~#airodump-ng --band a --channel 2 -- write output wlan0  
    > Feather you can see if interface is in monitor mode by typing this:  
    > root@kali:~#iwconfig wlan0  
    > wlan0 is an \[interface\]
    
6.  > **Here?s how to solve the wifi problem:  
    > This is how I managed it to work on ParrotOS with latest 5.3 kernels.  
    > This should also work with Kali Linux 2019.4 + latest kernels.**I also managed to get the TX-power to 30db. I will post instructions later today.  
    > Ok, one way to get it running is this:  
    > From clean ParrotOS 4.7 with all updates loaded:
    > 
    > 1.  go to /lib/firmware/
    > 2.  here you will need to create a folder named rtw88
    > 3.  go to /lib/firmware/rtlwifi/
    > 4.  here you will need to copy the file rtl8822befw.bin
    > 5.  go to /lib/firmware/rtw88/
    > 6.  here you will need to insert the file you just copied (rtl8822befw.bin)
    > 7.  now you will need to rename the file to rtw8822b\_fw.bin
    > 8.  reboot your system
    > 
    >   
    > Now your network manager should be able use your rtl8822be wifi adapter without any problems.  
    > Right now my ParrotOS has two bluetooth symbols in the task line but wifi is working.
    > 
    > Now I will try to correct the exta bluetooth symbol.
    > 
    >   
    > I?ll keep you up to date.  
    > veo
    
7.  ## repository not found
    
    > Hello,  
    > When i tried the above written code ,I am getting an error saying that 'repository not found' . any help to resolve this will be much appreciated.
    
8.  > Hello,  
    > when I tried the above code ,I am getting an error message "repository not found" any help to resolve this will be much appreciated.  
    > thanks
    
9.  > Monitor mode works fine that way, the problem is raven.. I find this that worked for me:
    > 
    > Code:
    > 
    > ```
    > apt-get purge --auto remove reaver
    > apt-get install sqlite3 lisqlite3-dev libcap0.8-dev
    > ```
    > 
    > then follow the steps for install reaver on [https://github.com/t6x/reaver-wps-fork-t6x](https://github.com/t6x/reaver-wps-fork-t6x)
    > 
    > Credits: zsecurity.org
    
10.  ## Increase Tx-Power and Driver Issues
    
    > hello all i have tried both method but none of them worked in my case . may be because of my wifi dongle is hardcoded so is there any way to set up txpower to 30 dbm  
    > and i have installed above mentioned drivers
    > 
    > Here is the Screenshot of my interference plz help
    
11.  > hello sir i have tried both method but none of them worked in my case . may be because of my wifi dongle is hardcoded so is there any way to set up txpower to 30 dbm
    > 
    > Here is the Screenshot of my interference plz help
    
12.  > bro send procedure to increase TX POWER to 30db  
    > as i cant achieve the 30db and my wifi mac changes everytime i connect also never shows the tx power by using command ::--> ifconfig  
    > here are my srcreeshots please help me out
    
13.  > Sir i need ur help to increase TX-POWER of TP-LINK T4U Archer AC 1300 wifi dongle ,it has fixed 12dbm tx-power and it also changes mac everytime i insert it here the commands
    > 
    > 1![](https://forums.kali.org/images/smilies/smile.png "Smile")
    > 
    > root@kali:~# iwconfig
    > 
    > lo no wireless extensions.
    > 
    > wlan0 unassociated Nickname:"<WIFI@REALTEK>"
    > 
    > Mode:Managed Frequency=2.412 GHz Access Point: Not-Associated
    > 
    > Sensitivity:0/0
    > 
    > Retry![](https://forums.kali.org/images/smilies/redface.png "Embarrassment")ff RTS thr![](https://forums.kali.org/images/smilies/redface.png "Embarrassment")ff Fragment thr![](https://forums.kali.org/images/smilies/redface.png "Embarrassment")ff
    > 
    > Encryption key![](https://forums.kali.org/images/smilies/redface.png "Embarrassment")ff
    > 
    > Power Management![](https://forums.kali.org/images/smilies/redface.png "Embarrassment")ff
    > 
    > Link Quality=0/100 Signal level=0 dBm Noise level=0 dBm
    > 
    > Rx invalid nwid:0 Rx invalid crypt:0 Rx invalid frag:0
    > 
    > Tx excessive retries:0 Invalid misc:0 Missed beacon:0
    > 
    > eth1 no wireless extensions.
    > 
    > eth0 no wireless extensions.
    > 
    > 2![](https://forums.kali.org/images/smilies/smile.png "Smile")
    > 
    > root@kali:~# iw dev
    > 
    > phy#2
    > 
    > Interface wlan0
    > 
    > ifindex 6
    > 
    > wdev 0x200000001
    > 
    > addr e6:14:4a:64:95:24
    > 
    > type managed
    > 
    > txpower 12.00 dBm
    > 
    > root@kali:~# iw dev
    > 
    > root@kali:~# iw dev
    > 
    > root@kali:~# iw dev
    > 
    > phy#3
    > 
    > Interface wlan0
    > 
    > ifindex 7
    > 
    > wdev 0x300000001
    > 
    > addr ae:b6:2f:9e:50:e1
    > 
    > type managed
    > 
    > txpower 12.00 dBm
    > 
    > root@kali:~#
    
14.  > ![Quote](https://forums.kali.org/images/misc/quote_icon.png "Quote") Originally Posted by **binukv** [![View Post](https://forums.kali.org/images/buttons/viewpost-right.png "View Post")](https://forums.kali.org/showthread.php?s=60e92a0902bbff5fd79993d5385640e4&p=89953#post89953)
    > 
    > Hello,  
    > when I tried the above code ,I am getting an error message "repository not found" any help to resolve this will be much appreciated.  
    > thanks
    > 
    > same here, I simply can find the repository
    
15.  > hello.
    > 
    > up to what version of kali does this code work?
    > 
    > i have installed kali 2020.3 and having a hard time installing this. asking for help.
    
16.  ## Code not working
    
    > Hi! i've tried using the code but it tells me to put username and password... Help please
    
17.  > it's not working for me ![](https://forums.kali.org/images/smilies/frown.png "Frown")
    
18.  > Is there any solution how to get Realtek 8811/12 USB wifi adapters to work in Kali 2020.4 ? I seem to find only solutions for old versions and plently of problems in the new one.
    > 
    > Which is the wifi adapter that is not having a neverending history of issues on kali?
    

#### Similar Threads

1.  Replies: 2
    
    Last Post: 2021-05-17, 01:35
    
2.  Replies: 0
    
    Last Post: 2021-01-13, 05:30
    

#### [![](https://forums.kali.org/images/buttons/collapse_40b.png)](https://forums.kali.org/showthread.php?44810-Realtek-RTL8812BU-Driver-for-Kali-Linux#top) Posting Permissions

-   You **may not** post new threads
-   You **may not** post replies
-   You **may not** post attachments
-   You **may not** edit your posts

-   [BB code](https://forums.kali.org/misc.php?s=60e92a0902bbff5fd79993d5385640e4&do=bbcode) is **On**
-   [Smilies](https://forums.kali.org/misc.php?s=60e92a0902bbff5fd79993d5385640e4&do=showsmilies) are **On**
-   [\[IMG\]](https://forums.kali.org/misc.php?s=60e92a0902bbff5fd79993d5385640e4&do=bbcode#imgcode) code is **On**
-   [\[VIDEO\]](https://forums.kali.org/misc.php?s=60e92a0902bbff5fd79993d5385640e4&do=bbcode#videocode) code is **On**
-   HTML code is **Off**

[Forum Rules](https://forums.kali.org/misc.php?s=60e92a0902bbff5fd79993d5385640e4&do=showrules)
> sudo,driver,rtl88x2bu,$ver,install,dkms,realtek,time,rtl8812bu,kali,running,rvhp,88x2bu,rsync,modprobe,build,/usr/src/rtl88x2bu-$ver,ifconfig,cheers,https://github.com/cilynx,repo,check,release,major,make,author,note,inject,packet,monitor,s/package_version=./1/p,8812bu,dkms.conf,installed,surely,issue,kernel,throw,felt,linux,4.19.28-2,ver=$sed,rtl88x2bu_wifi_linux_v5.3.1_27678.20180430_coex20180427-5959,https://github.com/cilynx/rtl88x2bu_wifi_linux_v5.3.1_27678.20180430_coex20180427-5959.git,clone,update,commands,writing,network,internet