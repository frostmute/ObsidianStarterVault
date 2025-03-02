---
created: 2025-02-18T23:06:06-06:00
reviewed:
url: "https://www.maketecheasier.com/compile-linux-programs-under-windows/"
title: "How to Compile Linux Programs Under Windows with Cygwin"
author:
  - "Gary Sims"
published: 2014-06-12
description: "Windows and Linux are two different systems, and to compile Linux programs under Windows is not an easy task. Luckily, there is a solution known as Cygwin."
---

#webclip/unread

# How to Compile Linux Programs Under Windows with Cygwin

Windows and Linux are two very different systems, and as such, it often isn’t easy to port programs written for one to the other, especially when dealing with GUI programs. Although there are many different cross-platform libraries and SDKs, native programs written without portability in mind are quite hard to port.

When it comes to compiling and running programs written for Linux on Windows, there is a solution known as Cygwin. The Cygwin project is a collection of the most common tools and compilers (including the bash shell and the GNU compiler chain) for Windows. It also includes a library that provides a compatibility layer so that programs which call Linux specific APIs can be compiled. Cygwin isn’t an emulator or virtual machine, and it doesn’t allow Linux binaries to run on Windows without first being re-compiled.

**Also read:** [How to Use the G++ Compiler on Linux](https://www.maketecheasier.com/use-g-plus-plus-compiler-linux/ "How to Use the G++ Compiler on Linux")

Visit the [Cygwin installation page](https://cygwin.com/install.html) and download the 32-bit or 64-bit setup executable (depending on which variant of Windows you are using). Execute the setup program. Click Next and Next again (to “Install from Internet”). The default directory is “C:\\cygwin”. It can be changed if needed, but unless you have a specific reason to change it, the default is best. Click Next, Next and Next again.

The Cygwin project has mirror sites all over the world; pick one which you think will best serve your location and click Next. You now need to pick which packages to install. To compile simple Linux programs in Windows, you will need the GNU Compiler Chain (GCC) which provides a C and C++ compiler.

![cygwin-select-packages](https://www.maketecheasier.com/assets/uploads/2014/06/cygwin-select-packages.jpg "cygwin-select-packages")

Type “gcc” in the search box and then click in the small plus sign next to “Devel” in the list of packages. Find “gcc-core” and “gcc-g++” and click “Skip” for each one. The word “Skip” will change into a version number and the “n/a” sign in the “Bin?” column will turn into a checked box. Type “make” in the search box and find “make” under “Devel.” Click “Skip” to mark it for install. Search for “wget” and also mark it for install from “Web.” To build the example below, we will also need “libiconv;” search for it and mark it for install.

![cygwin-gcc-selection](https://www.maketecheasier.com/assets/uploads/2014/06/cygwin-gcc-selection.jpg "cygwin-gcc-selection")

Click Next. The installer will then see what other packages need to be installed to resolve any dependencies. Click Next to accept the recommendations.

Once all the packages have been downloaded and installed, follow the last steps until the installer exits. Start the “Cygwin Terminal” to enter into the Linux-like development environment. In the terminal you don’t use Windows commands like “dir” but rather shell commands like “ls”.

To demonstrate how to compile a Linux program under Windows, we will use the [HTML-XML package](https://www.w3.org/Tools/HTML-XML-utils/README) from the W3. For a look at what it can do, see [How to Manipulate HTML and XML Files from the Command Line](https://www.maketecheasier.com/manipulate-html-and-xml-files-from-commnad-line/).

Download the source files using “wget”:

```
wget http://www.w3.org/Tools/HTML-XML-utils/html-xml-utils-6.7.tar.gz
```

Now unpack the archive file:

```
tar -zxf html-xml-utils-6.7.tar.gz
```

The source files are now in the “html-xml-utils-6.7” directory. Enter that directory:

Before the files can be built, you need to run the “configure” shell script to generate the Makefile (the build instructions) which are suitable for this build environment. This is a common step on Linux (and Cygwin) when building packages from source.

![cygwin-configure-html-utils](https://www.maketecheasier.com/assets/uploads/2014/06/cygwin-configure-html-utils.jpg "cygwin-configure-html-utils")

Once “configure” has finished, you can start the build using “make”:

The build will fail part way through. I was in two minds about what to do next. Either I could switch to another project and build that from its source or battle on with the HTML-XML-utils. I opted for the latter as it shows that not everything will be a walk-in-the-park when trying to compile Linux programs under Cygwin. The solution to this particular problem is simple. The error message shows that the linker is unable to find the “iconv” library. A quick look at the link command shows that the library isn’t specified. The quick and dirty solution is to run the command manually and tell the linker to use libconv. The “proper” way to fix this would be to start delving into the Makefile etc. to find out why it isn’t working.

![cygwin-build-fails](https://www.maketecheasier.com/assets/uploads/2014/06/cygwin-build-fails.jpg "cygwin-build-fails")

Run the following command, noting the inclusion of “-liconv” at the end:

```
gcc -g -O2 -o hxindex.exe hxindex.o scan.o html.o openurl.o url.o heap.o class.o errexit.o connectsock.o types.o tree.o genid.o dtd.o headers.o dict.o fopencookie.o -liconv
```

Once the “hxindex.exe” file is built, you can continue with the rest of the build by typing “make” again. The way “make” works is it checks what has and has not been built, and then it continues the build process at the appropriate point. Since we have manually built “hxindex.exe”, “make” just carries on with the next binary in its list.

When “make” completes, you will have all the .exe files in the html-xml-utils-6.7 directory.

If you get stuck using Cygwin you should look at the [FAQ](https://cygwin.com/faq.html), and at the [documentation](https://cygwin.com/cygwin-ug-net.html). Failing that, the project has a set of [mailing lists](https://cygwin.com/lists.html). If you have any problems with the steps described above, then please use the comments section below.