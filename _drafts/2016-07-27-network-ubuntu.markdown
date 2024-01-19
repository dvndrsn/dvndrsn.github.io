---
layout:   post
title:    "Ubuntu wireless problems"
subtitle: "Linux kernel and modules"
author:   "Dave Anderson"
date:     2016-07-27
---

After a perfect storm on Monday of an Ubuntu kernel update disabling wifi on my laptop (which doesn't have any other means to connect to the internet) and a literal storm knocking out the power (restored) and Internet (still out) that afternoon, I'm pretty much back in business, thanks to a [T-Mobile hotspot on my phone][tmobile] (so useful!) and [StackOverflow][solved]!

[tmobile]:https://support.t-mobile.com/docs/DOC-9847
[solved]:http://askubuntu.com/questions/760075/cant-view-wifi-networks-after-upgrading-to-ubuntu-16-04

[The solution][solved] involved [turning off SecureBoot][sb] in the system BIOS and unloading and re-loading modules using the below commands. Other steps to install packages weren't required as the drivers and other required software was already installed.

[sb]:https://neosmart.net/wiki/disabling-secure-boot/

Unload modules:

```
modprobe -r b43 bcma
modprobe -r brcmsmac bcma
modprobe -r wl
```

Reload modules:

```
modprobe wl
```

[Loadable Kernel Modules][lkm-history] are pieces of code that can be used to extend functionality of the Linux kernel dynamically without interruption at runtime. The Linux kernel is the lowest level piece of software on a computer that acts as an intermediary between user programs and the hardware. [Modules][arch-mod] are one way the architects of the system reduced the complexity and memory demands of the [core kernel][slack-kernel]. Typically when modules are changed while the system is active, such as through a system update, a program called [DKMS][ubuntu-dkms] ([Dynamic Kernel Module Support][dkms-reload]) will swap the updated module into the kernel automatically. However, when the kernel is updated, there may be incompatibilities which require to the module to be recompiled before it can be used (as happened to the [broadcom adapter][bcm-drivers] in this case).

[bcm-drivers]:https://help.ubuntu.com/community/WifiDocs/Driver/bcm43xx#Switching_between_drivers
[arch-mod]:https://wiki.archlinux.org/index.php/kernel_modules
[lkm-history]:http://www.tldp.org/HOWTO/html_single/Module-HOWTO/
[slack-kernel]:http://docs.slackware.com/slackbook:linux_kernelhttp://docs.slackware.com/slackbook:linux_kernel

[ubuntu-modules]:https://help.ubuntu.com/community/Loadable_Modules
[dkms-reload]:https://en.wikipedia.org/wiki/Dynamic_Kernel_Module_Support
[ubuntu-dkms]:https://help.ubuntu.com/community/DKMS

We can interact with loadable kernel modules through a couple of different commands in Ubuntu.

We can list all of the currently available modules by using `lsmod` which will show us the module name, size and number of dependencies.

```
onenote@onenote-lap:~$ lsmod | head
Module                  Size  Used by
binfmt_misc            20480  1
rfcomm                 69632  2
bnep                   20480  2
hid_multitouch         20480  0
dell_wmi               16384  0
dell_laptop            20480  0
dcdbas                 16384  1 dell_laptop
nls_iso8859_1          16384  1
intel_rapl             20480  0
```

We can also load a module using `insmod` or `modprobe`. [`Modprobe`][man-modprobe] is [smarter][how-mod-load] than `insmod` as it is able to leverage module dependencies calculated through the `depmod` command to make multiple calls to `insmod` to load the modules in the best order per the dependency graph.

[man-modprobe]:http://manpages.ubuntu.com/manpages/xenial/man8/modprobe.8.html
[wiki-modprobe]:https://en.wikipedia.org/wiki/Modprobe
[how-mod-load]:http://www.tldp.org/LDP/lkmpg/2.6/html/x44.html

Finally, we can remove a module from the kernel using `rmmod` or `modprobe -r`.

Hope this post helps demystify Linux Kernel Modules and related tools!

