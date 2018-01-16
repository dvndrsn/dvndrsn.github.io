---
layout:   post
title:    "Ubuntu Troubleshooting"
date:     2016-01-26
author:   "Dave Anderson"
subtitle: ""
---
When I started at the [Recurse Center][rc], I decided move my development activities from Windows to [Ubuntu][ubuntu1404]. Windows was always a cozy development environment for databases and Java, but Ubuntu made setup for everything such a breeze, including Python and the [Pydata][pydata] stack (which can be a [little][mingw] [tricky][python on win] to build on Windows due to C compiler dependencies, unless you're using a distribution like [Anaconda][anaconda]).

[Setting up Ubuntu][ubuntu setup] is generally a painless process, but there can be some quirks in the setup (especially when dual booting with Windows) and it helps to have some good references on hand to help walk through the problem. I'll share here some specific references that helped me understand and resolve one of the quirks I encountered. Specifically, I was experiencing a problem where the sound would not play back through the laptop speakers or headphones.

The Ubuntu community has great resources available including a sound troubleshooting [high level guide][sound] and [detailed procedure][sound proc]. This was really helpful in understanding the command line tools which are available to diagnose sound problems, however some additional research might be required once you notice something out of the ordinary. For me, I found that my sound card and driver was generally working fine, but the only available output was HDMI, even when no cable was plugged in! Some additional research yielded a [bug report][ubuntu bug] for my specific model on the Ubuntu launchpad. I also found the community wiki for [Arch Linux][dell arch] to be amazingly detailed for all sorts of configuration concerns. Even though this was for a different distribution of Linux, the configuration advice they provided was pretty spot-on, even for other configuration fixes I had taken care of previously.

Do you have any helpful resources you like to reference when troubleshooting linux or ubuntu problems? Shoot me a line!

[rc]: https://www.recurse.com/
[ubuntu1404]: http://www.ubuntu.com/download/desktop/install-ubuntu-desktop
[mingw]: http://www.mingw.org/wiki/howto_install_the_mingw_gcc_compiler_suite
[python on win]: http://docs.cython.org/src/tutorial/appendix.html
[pydata]: http://pydata.org/
[anaconda]: https://www.continuum.io/downloads

[ubuntu setup]:http://hgdev.co/installing-ubuntu-15-04-on-the-dell-xps-13-9343-2015-a-complete-guide-update/
[dual boot win ubuntu]:http://hgdev.co/install-ubuntu-15-10-on-the-dell-xps-13-9343-2015-a-complete-guide/

[sound]: https://help.ubuntu.com/community/SoundTroubleshooting
[sound proc]: https://help.ubuntu.com/community/SoundTroubleshootingProcedure
[ubuntu bug]: https://bugs.launchpad.net/ubuntu/+source/linux/+bug/1413446
[dell arch]: https://wiki.archlinux.org/index.php/Dell_XPS_13_(2015)
