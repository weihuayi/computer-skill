# Vim 高效技巧

## vim-orgmode 

enter `.vim/bundle/`

```
git clone https://github.com/tpope/vim-speeddating.git
```


```
git clone https://github.com/jceb/vim-orgmode.git
```

```
make vmb
```

```
vim orgmode.vmb
:so % # 在 vim 中执行， 结束后回车
```



## 命令行的 Normal 模式

进入命令行模式时, 按 `Ctrl+f` 会进入命令行模式的 Normal 模式, 可以使用 Normal 模式中
的常用命令.

## 删除文件中的重复行

```
:sort u
```
