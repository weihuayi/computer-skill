# 安装 Ubuntu 系统

下面是安装 Ubuntu 系统的基本配置

```
#! /bin/bash
# 系统配置
# 系统源更新

# 
apt-get -y update 

# 系统内核更新
apt-get -y dist-upgrade 

# 系统自带软件更新
 apt-get -y upgrade 

# python
 apt-get -y install python python-dev python3 python3-dev

# cmake 
# automake
sudo apt-get -y install cmake automake 

# fortran编译器gfortran 
sudo apt-get -y install build-essential gfortran 

# 版本控制软件:
# mercurial 
# subversion 
# git gitk 
sudo apt-get -y install mercurial subversion git gitk

# 并行库openmpi
sudo apt-get -y install openmpi-bin openmpi-common libopenmpi-dev

# 输入法
sudo apt-get install fcitx fcitx-tools fcitx-table-latex #这是用来输入Latex命令的吗

# 文档编译器texlive
sudo apt-get -y install texlive texlive-xetex texlive-math-extra texlive-science texlive-latex-extra texlive-fonts-extra texlive-lang-cjk

# 打包解压工具rar和unrar
# 图形处理软件gimp和inkscape
# vtk文件图形显示软件paraview
# 文献管理工具jabref
# pdf阅读批阅工具xournal
# 文档格式转换工具pandoc,把markdown转化为pdf
# 远程登录工具openssh-server
# xsel: 把 shell 中的命令输出到剪贴板
sudo apt-get -y install rar unrar gimp inkscape paraview xournal pandoc openssh-server xsel amule chromium-browser

#To enable the repository, follow the steps above to open the Other Software tab in Software & Updates.
#If you see the Canonical Partners repository in the list, make sure it is checked then close the Software & Updates window
apt-get install skype adobe-flushplugin


sudo apt-get install ctags vim-doc vim-scripts vim-nox-py2 



sudo apt-get install npm nodejs nodejs-dev nodejs-legacy 
sudo npm install -g gitbook
sudo apt-get install calibre ebook-speaker


#符号计算
sudo -E apt-add-repository ppa:aims/sagemath
sudo -E apt-get -y update
sudo -E apt-get -y install sagemath-upstream-binary

#支持独立显卡和集成显卡的切换
# 
sudo apt-add-repository ppa:graphics-drivers/ppa
sudo apt-get -y update
sudo apt-get install nvidia-364 nvidia-cuda-dev nvidia-settings nvidia-profiler nvidia-settings 

```




## 一些附加配置

1. 卸载 `ibus`

```
$ sudo apt-get remove ibus
```
2. 避免在 Terminal 中经常输入密码, 

```
$ sudo visudo # 打开 /etc/sudoers 文件
```

在文件的最后加入下面行

```
username ALL=(ALL) NOPASSWD: ALL
```

然后 `ctrl+x`, 编辑器会提示你保存，输入 `Y`后，会给一个建议的文件名 `sudoers.tmp`,
把 `.tmp` 删除，回车即可保存。


## 一些问题及解决办法

### No dash, No launcher, no top panel

有下面 5 种可能解决办法，用了 1, 2, 3, 5 解决了问题。 

1. Compiz Problems (OpenGL module not loading, Unity plugin not loading)
```
sudo rm -fr ~/.cache/compizconfig-1
sudo rm -fr ~/.compiz
```
2. Session not loading (Guest session loads fine)
```
sudo rm -fr ~/.Xauthority
sudo rm -fr ~/.config/autostart
```
3.  Session not loading (Guest not loading)
```
sudo apt-get install --reinstall ubuntu-desktop unity compizconfig-settings-manager upstart
```
4.  Launcher / Top Panel not loading (Nvidia cards)
```
sudo add-apt-repository ppa:xorg-edgers/ppa -y
sudo apt-get update
sudo apt-get install nvidia-340
sudo reboot
```
5. Clearing Unity
```
dconf reset -f /org/compiz/
setsid unity
```
