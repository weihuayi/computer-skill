# ubuntu 与 投影仪

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

