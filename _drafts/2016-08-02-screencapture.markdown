---
layout:   post
title:    "Screen Capture Tools on Ubuntu"
subtitle: "byzanz xdotool"
author:   "Dave Anderson"
date:     2016-08-02
---

`apt-get install byzanz`

```
corey@coreylaptop:~$ byzanz-record --help
Usage:
  byzanz-record [OPTION...] record your current desktop session

Help Options:
  -?, --help               Show help options
  --help-all               Show all help options
  --help-gtk               Show GTK+ Options

Application Options:
  -d, --duration=SECS      Duration of animation (default: 10 seconds)
  --delay=SECS             Delay before start (default: 1 second)
  -l, --loop               Let the animation loop
  -c, --cursor             Record mouse cursor
  -x, --x=PIXEL            X coordinate of rectangle to record
  -y, --y=PIXEL            Y coordinate of rectangle to record
  -w, --width=PIXEL        Width of recording rectangle
  -h, --height=PIXEL       Height of recording rectangle
  -v, --verbose            Be verbose
  --display=DISPLAY        X display to use
```

https://wiki.ubuntu.com/CreatingScreencasts

`apt-get install xdotool`

```
xdotool getmouselocation --shell
```

`byzanz-record -x $X -y $Y --width= --height= --cursor --verbose`

https://stackoverflow.com/questions/8480073/how-would-i-get-the-current-mouse-coordinates-in-bash
