# PHP:Hypertext Preprocessor

https://www.tutorialspoint.com/php/php_introduction.htm

1. 1994
1. 开源 


1. 服务器端的脚本语言, 嵌入在 HTML 网页中.
    * 管理动态内容
    * 数据库
    * 会话跟踪 (session tracking)
    * 构建整个商务网站
1. 流行的数据库基本都集成了 PHP
1. 执行敏捷快速
1. 支持大量的主要协议(protocals)
1. forgiving
1. PHP Syntax is C-like


用法:
1. 系统功能, 如创建, 打开, 读写和关闭操作系统中的文件
1. 处理表格, 从文件中收集数据, 保存数据到一个文件, 通过邮件可以发送数据,
   返回数据给用户
1. 通过 PHP 添加, 删除, 修改数据库中的元素
1. 访问 缓存(cookies)变量, 和设置缓存
1. 用 PHP 限止用户访问网站中的页面
1. 可以加密数据

特点:
1. 简单
1. 高效
1. 安全
1. 灵活
1. 熟悉

## Hello World

```
<html>
   
   <head>
      <title>Hello World</title>
   </head>
   
   <body>
      <?php echo "Hello, World!";?>
   </body>

</html>
```

```
<?php PHP code goes here ?>

<?    PHP code goes here ?>

<script language="php"> PHP code goes here </script>
```

## Escaping to PHP

1. 标准权威的写法:

```php
<?php ...?>
```

2. Short-open (SGML-style) tags

```
<?...?>
```

 需要在 php.ini 设置  `short_open_tag=ON`, 或者构建 PHP 时, 加入
`--enable-short-tags` 选项.

3. ASPstyle tags 

```
<% ... %>
```
需要在 php.ini 中设置 

4. HTML script tags

```
<script language="PHP"> ... </script>
```

### Comment

1. Single-line comments, begin with `#` or `//`.
1. Multi-lines printing, 
```
<?php
   # First Example
   print <<<END
   This uses the "here document" syntax to output
   multiple lines with $variable interpolation. Note
   that the here document terminator must appear on a
   line with just a semicolon no extra whitespace!
   END;
   
   # Second Example
   print "This spans
   multiple lines. The newlines will be
   output as well";
?>
```
1. Multi-lines comments
```
<?php
   /* This is a comment with multiline
      Author : Mohammad Mohtashim
      Purpose: Multiline Comments Demo
      Subject: PHP
   */
   
   print "An example with multi line comments";
?>
```

### whitespace insensitive 

### case sensitive

### statements and expressions terminated by semicolons

### Braces make blocks


## 变量 

变量在程序中的作用是存储信息.

1. 以 $ 开始
1. 变量的值是最近赋给它的值
1. =
1. 赋值之前可声明, 但不必要
1. 变量赋值之前有默认的值
1. PHP 在必要的时候自动进行类型转换
1. Perl like

注: 双引号中的变量会被它的值替换

```
<?php
    $channel = <<<_XML_
        This is a test 
    _XML_;

    echo <<<END
        test test test 
    END;
?>
```

**变量作用域**

1. 局部变量
1. 函数参数
1. 全局变量
1. 静态变量


**变量命名**

1. 以字母或下划线开头
1. 数字, 字母和下划线
1. 长度没有限止

## 常量

一个简单值的名字或标识.

1. 不能改变
1. 大小写敏感
1. 不能改变, 不能删除
1. `define()` 函数 
1. 不需要 $ 引用常量 
1. `constant()` 读取常量的值
1. 常量中只能包含 boolean integer, float, string

与变量的区别:
1. 没有 $
1. 常量只能用 `define()` 定义 


### Predefined  constant 

| 名字 | 意义 |
| :--- | :----|
| __LINE__| 文件的当前行 |
| __FILE__| 文件的绝对路径和文件名 |
| __FUNCTION__| 函数的名字 |
| __CLASS__ | 类名 |
| __METHOD__ | 类方法名 |

## 操作符

操作符: + * - / 
操作数: 4 5 

operator
operand

1. 算术操作符
1. 比较操作符
1. 逻辑操作符
1. 赋值操作符
1. 条件操作符或三元操作符 (ternary)


分类
1. 一元前缀操作符
1. 二元操作符
1. 条件操作符
1. 赋值操作符
unary
binary
ternary

## if 

## switch

## Loop

1. for  
2. while
3. do...while: 至少执行一次
4. foreach

## 数组 (Arrays)

1. 数值数组
1. 联合数组 (Associative array)


## 数组 (Arrays)

1. 数值数组
1. 联合数组 (Associative array)
1. 多维数组 

数组中的元素可以不一样吗? 应该可以

## 字符串

.

strlen
strpos


## web 概念

1. PHP 可以根据浏览器的类型, 提供动态的内容, 随机的生成数字, 或用户输入
1. 客户端浏览器如何被重定向 

1. $_PHP_SELF 
1. POST 方法 
1. HTTP header 

## GET & POST Method

有两种方式, 客户端浏览器可以发送信息给 web 服务器

浏览器先用 **URL encoding** 对信息编码

1. `+` 替换空格
1. 非字母字符用 16 进制数代替

### GET 方法 
GET 方法通过追加编码的用户信息到页面请求上, 来发送信息. 页面后面跟 `?`号, 再跟
```
name1=value1&name2=value2&name3=value3
```

1. GET 方法产生一个长字符串, 在你的服务日志, 和浏览器地址栏中
1. 最多 1024 个字符
1. 不要用 GET 方法发送敏感信息
1. 不能用来发送二进制信息给服务器, 如图像
1. 可以用 `QUERY_STRING` 环境变量获得信息.
1. PHP 提供 `$_GET` 联合数组访问 GET 方法发送的信息.

### POST 方法 
 
POST 通过 HTTP header 传送信息. 编码和 GET 方法一样, 但是放进一个 header 中,
header 名字叫 QUERY_STRING.

1. 数据大小无限止
1. 文本和二进制都可以
1. 安全性依赖 HTTP 协议, 使用安全的 HTTP, 可以保证你的信息是安全的.
1. PHP 提供 `$_POST` 联合数组来访问利用 POST 方法发送的信息.


### `$_REQUEST` 变量

该变量包含 `$_GET`, `$_POST`, 和 `$_COOKIE` 的内容. 

所以可以用它来访问上面三种方法的内容. 

## File Inclusion

你可以在服务器执行一个 PHP 文件之前, 把另一个 PHP 文件包含进来.

1. `include()`
1. `require()`

用处是帮助创建可以在多个页面中重用的
1. function
1. header
1. footer
1. element

### `include()`

会把指定文件的所有内容包含进来, 加载时出现问题, 会产生敬告, 但脚本还会继续执行.

### `require()`

`require` 与 `include` 的不同之处在于, 当加载出问题时, 会生成一个致命错误,
并停止脚本的运行

## Files & I/O

1. 打开文件: 
1. 读取文件: 
1. 写文件
1. 关闭文件

1. fopen
1. fread
1. fsize
1. fclose
1. fwrite

## Function 

1. Creating a PHP Function
1. Calling a PHP Function


传递引用
```
         function addSix(&$num) {
            $num += 6;
         }
```
返回值

```
return $sum;
```

默认参数
```
         function printMe($param = NULL) {
            print $param;
         }
```

动态函数调用

```
      <?php
         function sayHello() {
            echo "Hello<br />";
         }
         
         $function_holder = "sayHello";
         $function_holder();
      ?>
```

## 缓存 (Cookies)

1. 文本文件
1. 存储在客户计算机
1. 用于追踪

步骤
1. 服务器脚本一组缓存文件到浏览器. 如名字年龄, 标识号
1. 浏览器存储这些信息到本地, 以供未来使用
1. 下一次浏览器发送任何请求到服务器之后, 也会发送这些缓存信息到服务器,
   服务器用这些信识别用户
### 剖析缓存(The anatomy of a Cookie)

1. 缓存设在 HTTP header 中
1. JavaScript 也能设在浏览器中.

```
HTTP/1.1 200 OK
Date: Fri, 04 Feb 2000 21:03:38 GMT
Server: Apache/1.3.9 (UNIX) PHP/4.0b3
Set-Cookie: name=xyz; expires=Friday, 04-Feb-07 22:03:38 GMT; 
                 path=/; domain=tutorialspoint.com
Connection: close
Content-Type: text/html
```

如果浏览器配置了存储缓存, 它会存储这些信息直到过期.

```
GET / HTTP/1.0
Connection: Keep-Alive
User-Agent: Mozilla/4.6 (X11; I; Linux 2.2.6-15apmac ppc)
Host: zink.demon.co.uk:1126
Accept: image/gif, */*
Accept-Encoding: gzip
Accept-Language: en
Accept-Charset: iso-8859-1,*,utf-8
Cookie: name=xyz
```
浏览器的头可能内容如上.

PHP 脚本, 可以访问缓存, 这些信息存储在 `$_COOKIE` 或者 `$HTTP_COOKIE_VARS[]`.
如 `$HTTP_COOKIE_VARS["name"]` 这里的值应该为 xyz.

### Setting Cookies with PHP

1. setcookie()
1. 最多六个参数
1. 必须在 `<html>` tag 之前调用

```
setcookie(name, value, expire, path, domain, security);
```
1. Name: Cookie name
1. Value: 实际存储的信息.
1. expire: 过期的时间 00:00:00 GMT on 1st Jan 1970, 如果没认定,
   浏览器关闭时自动过期.
1. path: 指定某个目录下的缓存是有效的. `/` 表示对所有目录有效.
1. domain: 所有缓存都只对创建它们的 host and domain 有效
1. security: 1. 必须用 HTTPS 发送 0. 可以用常规的 HTTP

```
<?php
   setcookie("name", "John Watkin", time()+3600, "/","", 0);
   setcookie("age", "36", time()+3600, "/", "",  0);
?>
<html>
   
   <head>
      <title>Setting Cookies with PHP</title>
   </head>
   
   <body>
      <?php echo "Set Cookies"?>
   </body>
   
</html>
```

### PHP 访问缓存 

1. isset() 函数检查缓存是否设置.

```
      <?php
         if( isset($_COOKIE["name"]))
            echo "Welcome " . $_COOKIE["name"] . "<br />";
         
         else
            echo "Sorry... Not recognized" . "<br />";
      ?>
```

### PHP 删除缓存

设置一个过去的时间
```
<?php
   setcookie( "name", "", time()- 60, "/","", 0);
   setcookie( "age", "", time()- 60, "/","", 0);
?>
```

## PHP 会话

PHP 会话是另一种在整个网站多个网页间使数据可访问的方法.

会话在服务器的临时目录下创建文件, 保存会话变量和值. 在用户访问期间,
这个数据对所有网页来说都是 available.

通过 php.ini 文件中的 `session.save_path` 来设置目录 

1. PHP 首先创建一个唯一的标示符, 一个 32 位的随机 16 进制数.
1. 名为 `PHPSESSID` 的缓存文件自动发送给用户电脑, 数据为唯一的那个标示符.
1. 服务器在临时目录下自动创建一个会话文件, 文件名字格式为 `sess_标示符`.

PHP 脚本想重新获得会话变量中的值, 会自动从 PHPSESSID
缓存中获取那个唯一的标识符.

用户关闭了浏览器或离开了网站, 过了一个预定义的时间, 服务器自动终止会话,
通常是30分钟

## 开启 PHP 会话

1. `session_start`, 首先检查会话是否已经开启, 如果没有则开启一个会话
1. `session_start()` 调用放在页面的开始.
1. `$_SESSION[]` 联合数组中存储了会话变量
1. `isset[]` 检查一个进程变量是否已经设置.
1. `session_destroy()`, 无参数, 销毁所有会话变量
1. `unset()` 销毁某个会话变量
1. `php.ini` 中可自动设置启动一个会话, `session.auto_start=1`
1. 没有缓存的会话: 因为用户可能设置不允许存储缓存在他们的机器上. 会话开启时定义
   一个常量 `SID`
1. 打印 SID 时, 用 `htmlspecialchars()` 阻止 `XSS` 相关的攻击.


## PHP 发送邮件

1. `php.ini` 中设置
1. `[mail function]`, 主要 Unix 下
```
[mail function]
; For Win32 only.
SMTP = 

; For win32 only
sendmail_from = 

; For Unix only
sendmail_path = /usr/bin/sendmail -t -i
```
发送文本邮件:
1. `mail(to, subject, message, headers, parameters)`, 前面三个是必填参数. 
1. 调用即发, 成功返回 true , 失败返回 false
1. 可以指定多个收件人

发送 HTML 邮件:

发送带附件的邮件:

1. set `Content-type` header to `multipart/mixed`
1. 用 `boundaries` 指定文本和附件的内容.
1. `boundary` 以两个连字符(hyphens)后跟一个唯一的标识数字开始, 它不会出现在文件
    的消息部分.
1. `md5()` 会产生一个 32 位的 16 进制数, 比如 `md5(time())`
1. `final boudary` 必须以两个连字符结尾, 表示邮件的最后一个部分.

MIME (Multi-Purpose Internet Mail Extensions)
Simple Mail Transport Protocol o

## 上传文件

可以在 HTML form 中利用 PHP 脚本上传文件到服务器. 文件首先上传到一个临时目录下,
然后 PHP 脚本再移动到目标目录下.

`php.ini` 中设置:
1. `upload_tmp_dir`
1. `upload_max_filesize`

上传步骤:
1. 用户打开一个包含一个 HTML form 的页面, 文本框, a browse
   button and a submit button.
1. 用户点击 `browse` 按钮, 选择要上传的文件.
1. 文本框中出现要上传文件的全路径, 用户提交
1. HTML form 在动作属性中指定的 PHP 脚本检查文件是否已经到达,
   并且拷贝到目标目录.
1. PHP 向用户确认成功

上传的文件可以是文本, 图片, 或其它文档

## PHP 代码标准

1. Indenting and Line Length. tap 4 , 
1. Control Structures
```
if ((condition1) || (condition2)) {
   action1;
}elseif ((condition3) && (condition4)) {
   action2;
}else {
   default action;
}
switch (condition) {
   case 1:
      action1;
      break;
   
   case 2:
      action2;
      break;
         
   default:
      defaultaction;
      break;
}
```
1. Function Calls
```
$var = foo($bar, $baz, $quux);
```
1. Function Definitions: BSD/Allman style
```
function fooFunction($arg1, $arg2 = '') {
   if (condition) {
      statement;
   }
   return $val;
}
```
1. Comments: /* */ or //
1. PHP Code Tags: <?php ?>
1. Variable Names
    * use all lower case letters
    * Use '_' as the word separator
    * Global variables should be prepended with a 'g'
    * Global constants should be all caps with '_' separators
    * Static variables may be prepended with 's'
1. Make Functions Reentrant: 可重入, 不要保存静态变量
1. Alignment of Declaration Blocks.
1. One Statement Per LIne
1. Short Methods or Functions


## 预定义变量

PHP 超级全局变量

1. $GLOBALS
1. $_SERVER
1. $_GET
1. $_POST
1. $_FILES
1. $_REQUEST
1. $_COOKIE
1. $_SESSION
1. $_PHP_SELF
1. $php_errormsg

Server variables: $_SERVER

## 正则表达式

### POSIX 正则表达式
Range of characters
1. [0-9], [0-3]
1. [a-z]
1. [A-Z]
1. [a-Z]

1. p+: matches any string containing at least one p
1. p*: matches any string containing zero or more p's
1. p?: matches any string containing zero or more p's, just as p*
1. p{N}: Matches any string containing a sequence of N p's
1. p{2, 3}: matches any string containing a sequence of two or three p's.
1. p{2, }: matches any string containing a sequence of at least two p's
1. p$: it matches any string with p at the end of it
1. ^p: it matches any string with p at the beginning of it.

1. [^a-zA-z]: 
1. p.p:
1. ^.{2}$: matches any string containing exactly two characters.
1. <b>(.*)</b>
1. p(hp)*


### PERL Style 正则表达式

Meta characters:
1. . 一个字符
1. \s 空白字符
1. \S not \s

Meta characters:
1. . 一个字符
1. \s 空白字符
1. \S not \s
1. \d digit
1. \D  not \d
1. \w a word character
1. \W no-word character
1. [aeiou] matches a single character in the giver set
1. [^aeiou] matches a single character outside the given set 
1. (foo|bar|baz) matches any of alternatives specified

Modifiers:
1. i: makes the match case insensitive 
1. m: Specifies that if the string has newline or carriage return characters,
   the ^ and $ operators will now match against a newline boundary, instead of
   a string boundary
1. o: Evaluates the expression only once
1. s: Allows use of . t omatch a newline character
1. x: allows you to use white space in the expression for clarity
1. g: Globally finds all mathes
1. cg: Allows a search to continue even after a global match fails.


## Error & Exception Handing 

1. die()

### Defining Custom Error Handling Function

1. framework to define error handling function
1.`error_function(error_level,error_message, error_file,error_line,error_context); `
1. display_errors = ON 
1. log_errors = ON


## AJAX

AJAX stands for Asynchronous JavaScript and XML

AJAX is a new technique for creating better, faster, and more interactive web
applications with the help of XML, HTML, CSS and java Script

1. Conventional web application transmit information to and from the server
   using synchronous requests. 
