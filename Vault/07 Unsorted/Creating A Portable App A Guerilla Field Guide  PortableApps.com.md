---
created: 2025-02-12
source: https://portableapps.com/node/14868
banner: 
tags:
  - clippings
---

![Banner]()

***
Creating A Portable App: A Guerilla Field Guide

**Introduction:***Often, somebody will make a post asking for help. I wrote up a guide real quick for this poster, [here.](https://portableapps.com/node/14834) After a suggestion by r-andom, I re-posted as a forum topic. If you have a suggestion for the guide, post here. If you need help portablizing, make a new post in the [Portable App Development Forum.](https://portableapps.com/forums/development/portable_app_development) So, without much more text, I loose the gorilla. . .*

1.  Use the search box to find out if someone's done the work or some of the work for you. [Search PortableApps.com](https://portableapps.com/search).
2.  Become familiar with the launchers available. For instance:
    -   [X-Chat Portable](https://portableapps.com/node/10907) redirects the Path, and GTK directories.
    -   [Notepad++ Portable](https://portableapps.com/apps/development/notepadpp_portable) Moves files and then adjusts them so that any open files from your flash drive will now open on your new host.
    -   [7-Zip Portable](https://portableapps.com/apps/utilities/7-zip_portable) deals with the registry entries made by 7-zip.
    -   [PNotes Portable](https://portableapps.com/apps/office/pnotes_portable) Passes a command line variable to the program.
3.  Determine the license. Is it OSS or another type of license? If its [Open Source Software](http://en.wikipedia.org/wiki/Open_source_software), you can post all of the launcher and the program on the forums. Since PortableApps.com is dedicated to OpenSource software, its against the forum rules to post a piece of software that contains closed source (even if you are allowed to redistribute) software. If its closed source, well, you can post a launcher, similar to what I've done [here](https://portableapps.com/node/14387), ***only***. Why is this first? Well, you have to decide if its worth the work.
4.  Determine the programing language. Why? Well, you have to be careful. Is it done in:
    -   .Net? Sorry. While some don't care, alot of people here despise .Net, as its not installed on all computers. [See this link](https://portableapps.com/node/12730) For a whole discussion on the subject of .Net.
    -   Java? As I understand there's the [Java Portablizer](https://portableapps.com/apps/utilities/java_portable), but there is not yet an Open Source JRE. So use of Java applications is somehow limited.  
        You can study the following application to get an idea of portable Java implementation.
        
        -   [Eclipse Portable](https://portableapps.com/node/20219)
        -   [RSSOWl Portable](https://portableapps.com/node/19271)
5.  Get the tools. Load up- you'll need them.
    -   I whole heartedly suggest the use of [**HM NIS Edit (Portable)**](https://portableapps.com/node/13990) Select either the download with NSIS included, if you don't intend to download it separately, or without if you do. It adjusts properly in both occasions.
    -   Note also if you wish to use another editor, you can download a portable version of NSIS separately, [from here.](https://portableapps.com/apps/development/nsis_portable)
    -   **[Regshot](https://portableapps.com/node/10969).** which is used to figure out what changes a program made during the install process.
    -   Alternately, you can use [**Process Monitor**](https://portableapps.com/node/14387) to figure out what registry entries its reading.
    -   [NirSoft RegfromApp](http://www.nirsoft.net/utils/reg_file_from_application.html) is a small freeware utility that allows you to specify a specific process to monitor. You can even launch a process with it and monitor those specifically. It produces a nicer output of what registry entries the program has modified.
    -   I also suggest picking up [**Notepad ++ Portable.**](https://portableapps.com/apps/development/notepadpp_portable) Just in case.
    -   To handle making the icons, use something like [**IcoFx**](http://icofx.ro/files)
6.  Do your research. Read up on these topics in the forums:
    
    -   [The PortableApps Format Specifications](https://portableapps.com/development/portableapps.com_format)
    -   [The Official Installer](https://portableapps.com/apps/development/portableapps.com_installer)
    
    Feel your head is about to explode? Mine to, writing all this html. There's more ![Biggrin](Creating%20A%20Portable%20App%20A%20Guerilla%20Field%20Guide%20%20PortableApps.com/biggrin.gif)
    
7.  Download your program. If you have keyboard loggers, malware protection or anything that runs in the background, consider turning them off before taking a regshot. Now, fire up regshot and take a regshot of the computer by scanning the C drive, more on that in a minute, before installation. Go have a cup of coffee or a can of Mountain Dew. Don't touch the computer! You'll get extra registry entries.
8.  Install your program and run it a couple of times. Make sure you do this from a clean install. If you don't, you may have skewed results. Do NOTHING else during this time
9.  Take second regshot and then compare the results. Save it a html, it produces a nicer printout then .txt
10.  Figure out where the program is saving files. Check C:/Documents and Settings/UserName/Application Data for %appdata%. If you scan the entire C:\\ Drive with regshot, those changes should show up.
11.  What to do with registry entries:

-   **HKCU:**Regshot will show a HCKU modification as HKU\\Random Numbers\\whatever. Look for those in HKCU\\Software\\ and handle them in NSIS as `HKEY_CURRENT_USER\Software\Whatever`.
    
    -   Useful Entry: `HKU\S-1-5-21-1060284298-823518204-725345543-1003\Software\Texas Instruments\TI Connect\StartUp\`.
    -   Useless: HKU\\S-1-5-21-1060284298-823518204-725345543-1003\\Software\\Microsoft\\Windows\\ShellNoRoam\\MUICache
-   **HKLM:**HKLM is a branch of the registry that cannot be modified by someone with a Limited account- just an Administrator. Handle them by double checking that they are needed. Often, something like *InstallDir: whatever* can be ignored. Else-if those entries really really are needed, you will need to check that the launcher can do it, then launch the software. If you don't have the rights, you'll use a message box to say so and terminate the launcher. Handle them in NSIS as `HKEY_LOCAL_MACHINE\Software\whatever`
-   **HKU:** You can ignore these.

-   Find a base launcher that deals with those issues.
-   Adjust the launcher to reflect the changes you need made
-   Compile, test, and adjust
-   When it works, drop a note with it in the Beta Testing Forum., using this [format](https://portableapps.com/node/11965). Let us have at it. We'll be glad to ![Biggrin](Creating%20A%20Portable%20App%20A%20Guerilla%20Field%20Guide%20%20PortableApps.com/biggrin.gif)

Well, that about sums it up.

**More General Help**  
Open Source Software is generally found at [SourceForge](http://sourceforge.net/)  
You can get general help [here](https://portableapps.com/development)  
If you have any specific questions, give post, and we'll be happy to help.  
You can also join us at #portableapps on irc.freenode.net. You'll need a IRC client. You can use X-Chat, Pidgin, or Miranda. Helpful hints are [here.](https://portableapps.com/node/10951) Don't want to download a full blown IRC client? Well, I'm sure you will eventually, but [here's a web based IRC client](https://portableapps.com/support/chat) that's fast.

**Thanks to . . .**  
r-andom, for his blurb on java\\  
MaienM and Bart.S for letting me know about those pesky updates

*Changelog*

1.  10SEP08

-   Updated a few spelling issues
-   Added NirSoft RegfromApp
-   Updated link to installer thread
-   Changed up the way registry was talked about, added examples

-   08APR09

-   Add NSIS Portable to the Tools List

-   02OCT09

-   Add examples of Portable Java implementation
-   Update links to the PA.com format, Installer
-   Update link to NSIS Portable
