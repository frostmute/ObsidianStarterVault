---
cssclasses:
  - page-grid
  - pen-white
banner: "[[../03 - MEDIA & FILES/Pasted image 20241202105311.png]]"
---


![Pasted image 20241202105311](../03%20-%20MEDIA%20&%20FILES/Pasted%20image%2020241202105311.png)

<script>document.documentElement.className="client-js";RLCONF={"wgBreakFrames":!1,"wgSeparatorTransformTable":["",""],"wgDigitTransformTable":["",""],"wgDefaultDateFormat":"dmy","wgMonthNames":["","January","February","March","April","May","June","July","August","September","October","November","December"],"wgRequestId":"268f105de36676d5675377d2","wgCSPNonce":!1,"wgCanonicalNamespace":"","wgCanonicalSpecialPageName":!1,"wgNamespaceNumber":0,"wgPageName":"Aircrack-ng:_How_to_crack_WPA/WPA2_passwords","wgTitle":"Aircrack-ng: How to crack WPA/WPA2 passwords","wgCurRevisionId":14641,"wgRevisionId":14641,"wgArticleId":1644,"wgIsArticle":!0,"wgIsRedirect":!1,"wgAction":"view","wgUserName":null,"wgUserGroups":["*"],"wgCategories":["Documentation","Pentesting"],"wgPageContentLanguage":"en","wgPageContentModel":"wikitext","wgRelevantPageName":"Aircrack-ng:_How_to_crack_WPA/WPA2_passwords","wgRelevantArticleId":1644,"wgIsProbablyEditable":!1,"wgRelevantPageIsProbablyEditable":!1,
"wgRestrictionEdit":[],"wgRestrictionMove":[]};RLSTATE={"site.styles":"ready","noscript":"ready","user.styles":"ready","user":"ready","user.options":"loading","skins.vector.styles.legacy":"ready"};RLPAGEMODULES=["site","mediawiki.page.ready","mediawiki.toc","skins.vector.legacy.js"];</script>
<script>(RLQ=window.RLQ||[]).push(function(){mw.loader.implement("user.options@1hzgi",function($,jQuery,require,module){/*@nomin*/mw.user.tokens.set({"patrolToken":"+\\","watchToken":"+\\","csrfToken":"+\\"});
});});</script>
<link rel="stylesheet" href="/load.php?lang=en&amp;modules=skins.vector.styles.legacy&amp;only=styles&amp;skin=vector"/>
<script async="" src="/load.php?lang=en&amp;modules=startup&amp;only=scripts&amp;raw=1&amp;skin=vector"></script>
<meta name="generator" content="MediaWiki 1.37.2"/>
<meta name="format-detection" content="telephone=no"/>
<link rel="shortcut icon" href="/favicon.ico"/>
<link rel="search" type="application/opensearchdescription+xml" href="/opensearch_desc.php" title="Embedded Lab Vienna for IoT &amp; Security (en)"/>
<link rel="EditURI" type="application/rsd+xml" href="https://wiki.elvis.science/api.php?action=rsd"/>
<link rel="alternate" type="application/atom+xml" title="Embedded Lab Vienna for IoT &amp; Security Atom feed" href="/index.php?title=Special:RecentChanges&amp;feed=atom"/>
</head>
<body class="mediawiki ltr sitedir-ltr mw-hide-empty-elt ns-0 ns-subject page-Aircrack-ng_How_to_crack_WPA_WPA2_passwords rootpage-Aircrack-ng_How_to_crack_WPA_WPA2_passwords skin-vector action-view skin-vector-legacy"><div id="mw-page-base" class="noprint"></div>
<div id="mw-head-base" class="noprint"></div>
<div id="content" class="mw-body" role="main">
	<a id="top"></a>
	<div id="siteNotice"></div>
	<div class="mw-indicators">
	</div>
	<h1 id="firstHeading" class="firstHeading" >Aircrack-ng: How to crack WPA/WPA2 passwords</h1>
	<div id="bodyContent" class="vector-body">
		<div id="siteSub" class="noprint">From Embedded Lab Vienna for IoT &amp; Security</div>
		<div id="contentSub"></div>
		<div id="contentSub2"></div>
		
		<div id="jump-to-nav"></div>
		<a class="mw-jump-link" href="#mw-head">Jump to navigation</a>
		<a class="mw-jump-link" href="#searchInput">Jump to search</a>
		<div id="mw-content-text" class="mw-body-content mw-content-ltr" lang="en" dir="ltr"><div class="mw-parser-output"><div id="toc" class="toc" role="navigation" aria-labelledby="mw-toc-heading"><input type="checkbox" role="button" id="toctogglecheckbox" class="toctogglecheckbox" style="display:none" /><div class="toctitle" lang="en" dir="ltr"><h2 id="mw-toc-heading">Contents</h2><span class="toctogglespan"><label class="toctogglelabel" for="toctogglecheckbox"></label></span></div>
<ul>
<li class="toclevel-1 tocsection-1"><a href="#Summary"><span class="tocnumber">1</span> <span class="toctext">Summary</span></a></li>
<li class="toclevel-1 tocsection-2"><a href="#Requirements"><span class="tocnumber">2</span> <span class="toctext">Requirements</span></a></li>
<li class="toclevel-1 tocsection-3"><a href="#Description"><span class="tocnumber">3</span> <span class="toctext">Description</span></a>
<ul>
<li class="toclevel-2 tocsection-4"><a href="#How_to_use_aircrack-ng_for_cracking"><span class="tocnumber">3.1</span> <span class="toctext">How to use aircrack-ng for cracking</span></a></li>
<li class="toclevel-2 tocsection-5"><a href="#Used_Hardware"><span class="tocnumber">3.2</span> <span class="toctext">Used Hardware</span></a></li>
<li class="toclevel-2 tocsection-6"><a href="#Step_1"><span class="tocnumber">3.3</span> <span class="toctext">Step 1</span></a></li>
<li class="toclevel-2 tocsection-7"><a href="#Step_2"><span class="tocnumber">3.4</span> <span class="toctext">Step 2</span></a></li>
<li class="toclevel-2 tocsection-8"><a href="#Step_3"><span class="tocnumber">3.5</span> <span class="toctext">Step 3</span></a></li>
<li class="toclevel-2 tocsection-9"><a href="#Step_4"><span class="tocnumber">3.6</span> <span class="toctext">Step 4</span></a></li>
</ul>
</li>
<li class="toclevel-1 tocsection-10"><a href="#Other_Guides"><span class="tocnumber">4</span> <span class="toctext">Other Guides</span></a></li>
<li class="toclevel-1 tocsection-11"><a href="#References"><span class="tocnumber">5</span> <span class="toctext">References</span></a></li>
</ul>
</div>

<h2><span class="mw-headline" id="Summary">Summary</span></h2>
<p>This documentation is a step-by-step guide explaining how to use the aircrack-ng program suite to crack passwords of Wireless Access Points using WPA or WPA2. The guide is meant for usage on *NIX systems capable of installing and running aircrack-ng. Results are based on tests that were run on the Kali Linux custom image for VMware (Kali Linux 2020.4 64bit) wich is maintained and provided by Offensive Security <a rel="nofollow" class="external autonumber" href="https://images.kali.org/virtual-images/kali-linux-2020.4-vmware-amd64.7z">[1]</a>. The used client software was VMware Workstation Pro 16.1.0 build-17198959 and the used host system was Windows 10 Home Edition (64 bit).   
</p>
<h2><span class="mw-headline" id="Requirements">Requirements</span></h2>
<ul><li>Operating system: Kali Linux</li>
<li>Packages: aicrack-ng program suite</li></ul>
<p>If you want to install aircrack-ng from source, click here <a rel="nofollow" class="external autonumber" href="https://www.aircrack-ng.org/doku.php?id=install_aircrack">[2]</a> to access the official documentation.
</p><p>On the image that was used (Kali Linux 2020.4 64bit for VMware by Offensive Security), the aicrack-ng program suite is already preinstalled. Just type <b>sudo aircrack-ng</b> in the shell to get an overview of available options. You will only need a few specific programs and options for cracking WPA/WPA2 PSK, which are explained in the following sections.
</p>
<h2><span class="mw-headline" id="Description">Description</span></h2>
<p>If you want to learn more about the inner workings of aicrack-ng's WPA/WPA2 PSK cracking, you can read more on the section about <a href="/index.php?title=Password_Cracking" title="Password Cracking">Password Cracking</a>.
</p><p>Before we get down to the nitty-gritty, there is some information that has to be known to be able to "get cracking".
</p><p>What we need:
</p>
<pre> MAC address of machine running aircrack-ng suite
 MAC address of wireless client using WPA/WPA2
 BSSID (MAC address of victim access point)
 ESSID (Wireless network name)
 Access point channel number
 Wireless interface name
</pre>
<p>We need all of this to fill out the necessary portions of the following commands.
</p><p>The guide itself was summarized from official documentation <a rel="nofollow" class="external autonumber" href="https://www.aircrack-ng.org/doku.php?id=cracking_wpa">[3]</a> and tested in my home network.
</p><p><b>Disclaimer: The following guide must not be used on networks without permission. Doing so is illegal and can result in criminal charges.</b>
</p>
<h3><span class="mw-headline" id="How_to_use_aircrack-ng_for_cracking">How to use aircrack-ng for cracking</span></h3>
<pre> 1. Start the wireless interface in monitor mode on the specific AP channel
 2. Start airodump-ng on AP channel with filter for bssid to collect authentication handshake
 3. Use aireplay-ng to deauthenticate the wireless client
 4. Run aircrack-ng to crack the pre-shared key using the authentication handshake
</pre>
<h3><span class="mw-headline" id="Used_Hardware">Used Hardware</span></h3>
<p>Before we start, there is one thing more that needs to be addressed. To be able to capture and inject packets, it is neccessary to put the network interface card (NIC) of the machine running the aircrack-ng program suite into so called "promiscuous mode". In general, NICs do not use this mode, as they do not need to read packets that are not addressed to them. Since we are trying to do something "out of the ordinary" here (e.g. capture all network traffic and inject our own packets) we can only succeed if our NIC knows that it should do exactly that.
</p><p>This can be done by either manually updating the drivers <a rel="nofollow" class="external autonumber" href="https://www.aircrack-ng.org/doku.php?id=patching">[4]</a>, which can be quite cumbersome, or by buying a Wireless USB Adapter using a chipset that is supported by the machine running the aircrack-ng suite. In our special case, we do not even have the freedom of doing our own dirty work - according to Kali Linux official documentation regarding virtual machines, we are forced to use an adapter, as patching only works in a native environment.
</p><p>The problem is that a lot of products are available who promise to do what we want, but not a lot of them actually work. Oftentimes, chipsets are not compatible with Kali Linux, which would make the device unusable for our purposes. For this specific documentation, the USB Wireless Adapter "Panda Wireless PAU05" for 802.11n was used, and the product version was 2.6.15. If you use this device, you should be fine - but only in 2.4 Ghz range. Also, high digit channels like 111 are not supported. Sorry!
</p><p>If you want to be 100% sure if your device is up to the job, you can manually test injection capabilities by entering the following commmand in the shell:
</p>
<pre> <b>sudo aireplay-ng -9 -e &lt;ESSID&gt; -a &lt;BSSID&gt; &lt;interface&gt;</b>
	 -9 means injection test
	 -e is the wireless network name that is shown (ESSID)
	 -a is the MAC address of the victim access point (BSSID)
	 &lt;interface&gt; is the wireless interface name from the machine you are running aircrack-ng on
</pre>
<h3><span class="mw-headline" id="Step_1">Step 1</span></h3>
<p>Use airmon-ng to disable the network-manager service and prevent it from overwriting our settings, and to start capturing traffic on the channel used by the victim AP.
</p><p>Enter these commands in the shell
</p>
<pre> <b>sudo airmon-ng check kill</b>
 <b>sudo airmon-ng start &lt;interface&gt; &lt;channel&gt;</b>
</pre>
<h3><span class="mw-headline" id="Step_2">Step 2</span></h3>
<p>Start airodump-ng on the AP channel to collect the 4-way-handshake (only occurs when a client connects to the AP)
</p><p>Enter this command in the shell
</p>
<pre> <b>sudo airodump-ng -c &lt;channel&gt; --bssid &lt;BSSID&gt; -w psk &lt;interface&gt;</b>
	 -c is the number of the channel used by the wireless access point
	 --bssid is the MAC address of the victim access point. This eliminates extraneous traffic.
	 -w psk is the file name prefix for the file which will contain the IVs. Captured files are saved automatically to the folder you run aircrack-ng from.
	 &lt;interface&gt; is the interface name.
</pre>
<h3><span class="mw-headline" id="Step_3">Step 3</span></h3>
<p>Use aireplay-ng to deauthenticate AP client. You need this to force it to reconnect if it was already connected to the AP when you started capturing traffic. You need the 4-way-handshake for cracking, and if you do not deauthenticate the client by force (through packet injection) you will have to wait until it disconnects and reconnects again, which can take a long time, or maybe will not happen at all. This is why you need a NIC or Adapter that is capable of packet injection.
</p><p>Enter this command in the shell
</p>
<pre> <b>sudo aireplay-ng -0 1 -a &lt;BSSID&gt; -c &lt;client&gt; &lt;interface&gt;</b>
	 -0 means deauthentication
	 1 is the number of deauths to send (you can send multiple if you wish)
	 -a is the MAC address of the victim access point
	 -c is the MAC address of the wireless client you are deauthing
	 &lt;interface&gt; is the interface name
</pre>
<h3><span class="mw-headline" id="Step_4">Step 4</span></h3>
<p>Run aircrack-ng to start a dictionary attack on the PCAP file (the file containing all the captured packets).
</p><p>Enter this command in the shell
</p>
<pre> <b>sudo aircrack-ng -w /link/to/passwordlist -b &lt;BSSID&gt; psk*.cap</b>
	 -w is the full path to the dictionary file used for cracking. You don't need to specify full path if the file is located in the same directory.
	 *.cap is the extension of files containing captured packets. Through usind the wildcard * all files are included that have the *.psk ending.
</pre>
<p>Important: You need to use a dictionary attack to be able to crack WPA/WPA2 passwords. Brute forcing does not work. Cracking WPA/WPA2 passwords after getting the 4-way-handshake will only work if the password is in the list. If the victim AP makes use of a randomly generated password of a certain (large) size, our chances of getting the password will be next to nil. So always choose a robust password for your own setup, to make evil hackers lifes miserable!
