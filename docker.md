# Docker

## Docker 是什么?

Docker 是一个开源的应用容器引擎,
让开发者可以打包他们的应用以及依赖包到一个可移植的容器中,

**Image** 是一个文件系统, 包含运行时需要的相应参数.
**Container** 就是一个 Image 的运行实例.

An image is a filesystem and parameters to use at runtime. It doesn’t have state and never changes. A container is a running instance of an image.

## 安装
```
$ sudo apt-get update
$ sudo apt-get install apt-transport-https ca-certificates
$ sudo apt-key adv --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 58118E89F3A912897C070ADBF76221572C52609D
$ sudo echo 'deb https://apt.dockerproject.org/repo ubuntu-xenial main'  > /etc/apt/sources.list.d/docker.list
$ sudo apt-get update
$ sudo apt-get purge lxc-docker # purge 净化
$ apt-cache policy docker-engine
$ sudo apt-get install linux-image-extra-$(uname -r) linux-image-extra-virtual
$ sudo apt-get update
$ sudo apt-get install docker-engine
$ sudo service docker start
$ sudo docker run hello-world
```

## 使用


