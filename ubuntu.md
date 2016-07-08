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


