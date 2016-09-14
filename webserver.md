# 搭建网络服务器

# 安装相关软件

```
$ sudo apt-get install apache2
$ sudo apt-get install mysql-common mysql-server mysql-client
$ sudo apt-get install php7.0-fpm php7.0-mysql php7.0-common php7.0-mbstring php7.0-gd php7.0-json php7.0-cli php7.0-curl libapache2-mod-php7.0
$ service apache2 start
$ service mysql start
$ service mysql status
```

设置开机自动

```
sudo systemctl enable mysql
sudo systemctl enable apache2
```

编译 ngrok
https://imququ.com/post/self-hosted-ngrokd.html

```
git clone https://github.com/tutumcloud/ngrok.git ngrok
cd ngrok
```

```
NGROK_DOMAIN="imququ.com"

openssl genrsa -out base.key 2048
openssl req -new -x509 -nodes -key base.key -days 10000 -subj "/CN=$NGROK_DOMAIN"
-out base.pem
openssl genrsa -out server.key 2048
openssl req -new -key server.key -subj "/CN=$NGROK_DOMAIN" -out server.csr
openssl x509 -req -in server.csr -CA base.pem -CAkey base.key -CAcreateserial -days
10000 -out server.crt

cp base.pem assets/client/tls/ngrokroot.crt
```

```
sudo make release-server release-client
```

PHP（“PHP: Hypertext Preprocessor”，超文本预处理器的字母缩写）是一种被广泛应用的开
放源代码的多用途脚本语言，它可嵌入到HTML中，尤其适合 web 开发。

cURL是一个利用URL语法在命令行下工作的文件传输工具，1997年首次发行。它支持文件上传和
下载，所以是综合传输工具，但按传统，习惯称cURL为下载工具。cURL还包含了用于程序开发的libcurl。
