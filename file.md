# 文件及文件夹的处理技巧

## Pdf 图片的剪裁

当手头的 Pdf 图片边上有很多空白时, 可以用 Texlive 中的 `pdfcrop` 命令剪裁

首先要安装 Texlive 的辅助程序包, 里面有很多有用的小程序

```
$ sudo apt-get install texlive-extra-utils
```

```
$ pdfcrop  fig.pdf
```
[1](http://examplenow.com/zh-cn/package/texlive-extra-utils/

## pdf或其它图片的合并

```
pdfjoin 1.pdf 2.pdf ...
```
