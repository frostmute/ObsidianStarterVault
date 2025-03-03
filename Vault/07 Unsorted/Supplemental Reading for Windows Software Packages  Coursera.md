---
banner: https://s3.amazonaws.com/coursera/media/Grid_Coursera_Partners_updated.png
created: 2024-06-17T10:38:19
source: https://www.coursera.org/learn/os-power-user/supplement/Smg89/supplemental-reading-for-windows-software-packages
author: 
cssclasses:
  - dashboard
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
title: "Supplemental Reading for Windows Software Packages | Coursera"
description: "In the third module of this course, we'll learn about package and software management in Windows and Linux OS. It's important to know how package installs work and how devices and drivers are managed within these operating systems. We will also ..."
host: www.coursera.org
image: https://s3.amazonaws.com/coursera/media/Grid_Coursera_Partners_updated.png
```
# Supplemental Reading for Windows Software Packages

# Windows Software Packages

Developers have different ways to package software using software compiling tools. In Windows, software is usually packaged as a .exe (executable file). Windows software can be sourced from the Microsoft Store or downloaded directly and installed in several ways. This reading covers the most common methods software packages are installed on Windows OS.

# Installation Package

Installation packages contain all the information the Windows Installer needs to install software on a computer. The packages include a .msi file (Microsoft install file) which contains an installation database, summary information, and data streams for each part of the installation. The .msi file may also include internal source files and external source files needed for the installation. Windows Installer uses the information contained in the .msi file to install, maintain, and remove programs on Windows. 

## Portable Executable

These .msi files are contained within a portable executable (PE), which is a format specific to Windows. The file type extension for a PE is .exe. Although these PEs commonly include instructions for the computer to run, such as the .msi files, they may also have images that the program may run or computer code.

# Self-extracting Executable

While it is common to install software using the Windows Installer, it is helpful for you to know how to install software using the command line.

Self-extractor packages are executable files (.exe) that are run in the Windows interface by clicking on them or running from the command line. Software installed by an IT professional onto an end user’s computer will likely use this format. Software installation package, update package, or hotfix package created with the Microsoft Self-Extractor, can be executed using the following command lines: 

-   **/extract:\[path\]**: Extracts the content of the package to the path folder. If a path isn’t specified, then a Browse dialog box appears.
    
-   **/log:\[path to log file\]**: Enables verbose logging (more detailed information recorded in the log file) for the update installation.
    
-   **/lang:lcid**: Sets the user interface to the specified locale when multiple locales are available in the package.
    
-   **/quiet**: Runs the package in silent mode.
    
-   **/passive**: Runs the update without any interaction from the user.
    
-   **/norestart**: Prevents prompting of the user when a restart of the computer is needed.
    
-   **/forcerestart**: Forces a restart of the computer as soon as the update is finished.
    

You can always type **/?**, **/h**, or **/help** from the command line to view these options. 

# App Packager

The app packager used in the Windows Software Development Kit (SDK) and Microsoft Visual Studio includes a program called MakeAppx.exe. MakeAppx.exe is a tool that creates an app package from files on disk or extracts the files from an app package to disk. For Windows 8.1 and higher, this program can also create and extract app package bundles. This tool is primarily used by software developers. 

# Microsoft Store

The Microsoft Store, included in the Windows OS, is the primary source for apps, games, and videos in Windows. The Microsoft Store only contains apps and programs certified for compatibility and curated for content. Software installed through the Microsoft store is automatically updated by default. Some organizations may disable the Microsoft store on user computers to limit users’ ability to install new applications without authorization. 

While the Microsoft Store is a convenient and popular way to get programs on Windows, some software can also be downloaded directly from developers.

# Key takeaways

Windows has many different ways to distribute, install, uninstall, and update programs and code on a computer. Depending on the organization, IT might use any of these installation options regularly.

-   Installation packages contain all the information the Windows Installer needs to install software on a computer.
    
-   While it is common to install software using the Windows Installer, it is helpful for you to know how to install software using the command line.
    
-   The Windows Software Development Kit (SDK) and Microsoft Visual Studio include a program called MakeAppx.exe. MakeAppx.exe is a tool that creates an app package from files on disk or extracts the files from an app package to disk.
    
-   Microsoft Store is a digital distribution storefront for apps, games, and other media.
    

# Resources for more information

-   Installation Package: [https://docs.microsoft.com/en-us/windows/win32/msi/installation-packageOpens in a new tab](https://docs.microsoft.com/en-us/windows/win32/msi/installation-package)
    
-   App packager (MakeAppx.exe): [https://docs.microsoft.com/en-us/windows/win32/appxpkg/make-appx-package--makeappx-exe-Opens in a new tab](https://docs.microsoft.com/en-us/windows/win32/appxpkg/make-appx-package--makeappx-exe-)
    
-   Portable Executables: [https://docs.microsoft.com/en-us/windows/win32/debug/pe-formatOpens in a new tab](https://docs.microsoft.com/en-us/windows/win32/debug/pe-format)
    

-   Self-extractor: [https://docs.microsoft.com/en-us/troubleshoot/windows-client/deployment/command-switches-supported-by-self-extractor-package](https://docs.microsoft.com/en-us/troubleshoot/windows-client/deployment/command-switches-supported-by-self-extractor-package)
> 