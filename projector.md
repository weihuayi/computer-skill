# ubuntu 与 投影仪

RandR ("resize and rotate") is a communications protocol written as an
extension to the X11[2] protocol. XRandR provides the ability to resize, rotate
and reflect the root window of a screen. RandR is also responsible for setting
the screen refresh rate.

xrandr is an official configuration utility to the RandR X Window System
extension. It can be used to set the size, orientation or reflection of the
outputs for a screen. For configuring multiple monitors see the Multihead page
An implementation of RandR is part of the X.Org Server.[3]

A user can typically use applications with a graphical front-end provided by
the desktop environment to control RandR, but the additional command line tool
xrandr exists. xrandr tells the display controller what resolution and refresh
rate it should output on which of its outputs (e.g. VGA1, HDMI3). The name of
the output is determined by the device driver for the display controller (KMS
driver).



`xrandr` 命令行可以很方便地切换双屏，常用方式如下，其他的可以自己探索：

1. 打开外接显示器(最高分辨率)，与笔记本液晶屏幕显示同样内容（克隆）
```
$ xrandr --output VGA --same-as LVDS --auto
```
1. 打开外接显示器(分辨率为1024x768)，与笔记本液晶屏幕显示同样内容（克隆）
```
$ xrandr --output VGA --same-as LVDS --mode 1024x768
```
1. 打开外接显示器(最高分辨率)，设置为右侧扩展屏幕
```
xrandr --output VGA --right-of LVDS --auto
```
1. 关闭外接显示器
```
xrandr --output VGA --off
```
1. 打开外接显示器，同时关闭笔记本液晶屏幕（只用外接显示器工作）
```
xrandr --output VGA --auto --output LVDS --off
```
1. 关闭外接显示器，同时打开笔记本液晶屏幕 (只用笔记本液晶屏)
```
xrandr --output VGA --off --output LVDS --auto
```

转贴：http://www.alterego7.com/2008/04/getting-projectors-to-work-in-ubuntu.html

1. Connect the projector to your laptop. 
2. Do this in command line.

sudo dpkg-reconfigure xserver-xorg

3. Just press Enter through every screen. 
4. Restart X for the changes to take effect by pressing CTRL + ALT + BACKSPACE. 
5. Log in again as you always do. 
6. And finally, the projector will automagically display your Ubuntu desktop
   and you can show off your desktop effects to your co-workers.

