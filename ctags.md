# ctags


## 存在问题

1. 如何利用 Git 的 hook 功能，使得在 `git commit` 之后， 自动调用 `ctags` 更新
   `tags`.
2. 如何自动跳转到第三方依赖库，查看相关信息。

## ctags 简介


## 基本用法

在你的代码主目录中，运行如下命令：

```
$ ctags --extra=+f -R --exclude=@.ctagsignore .
```

其中 
* `--extra=+f`, 表示生成文件跳转的信息
* `-R`, 表示递归生成子目录中文件 tag 信息
* `--exclude=@.ctagsignore`, 表示不生成文件 `.ctagsignore` 中所列目录或文件的 tag
    信息。
* `.`, 表示当前目录。


运行完上述命令，在你的代码主目录中就会出现名为 `tags` 的文件。 

在 `vim` 中命令行模式， 输入 `:tag file_name`， 即可跳转到相应文件。`ctrl+t`
就跳会原来位置。

其它的命令[1]：

```
:tag TAB            - list the known tags
:tag function_name  - jump to that function
ctrl-t   - goes to previous spot where you called :tag
ctrl-]   - calls :tag on the word under the cursor        
:ptag    - open tag in preview window (also ctrl-w })
:pclose  - close preview window
```

[1] https://www.cs.oberlin.edu/~kuperman/help/vim/tags.html


