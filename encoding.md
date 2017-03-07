## VIM 打开 GBK 编码文件不乱码

```
sudo vi /var/lib/locales/supported.d/zh
```

加入 

```
zh_CN.GBK GBK
```

运行 

```
sudo locale-gen
```

在 `.vimrc` 中加入如下设置：

```
set encoding=utf-8
set fileencoding=utf-8, GBK
```
