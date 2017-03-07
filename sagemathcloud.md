# SageMathCloud 


### Docker 

下面的命令启动一个名字为 `smc` 容器, 通过端口 8080 访问, 数据存储在家目录中,
这样方便后面更新 SageMathCloud, 
```
$ sudo docker run --name=smc -v ~/smc:/projects -d -p 8080:80 williamstein/sagemathcloud
```

其中 `-v` 参数可指定一个 Host 的文件夹做为数据的存储文件夹, 这样即使 Container
被删除时, 这个文件中数据也会保存.

https://docs.docker.com/engine/userguide/networking/default_network/dockerlinks/

布署最新的 Image
```
$ sudo docker rm smc # delete container with name `smc`
$ suod docker images # list all images 
$ sudo docker rmi williamstein/sagemathcloud
$ sudo docker pull williamstein/sagemathcloud 
$ sudo docker run --name=smc -v ~/smc:/projects -d -p 8080:80 williamstein/sagemathcloud

```

执行如下命令进入名字为 `smc` 的容器的命令行界面, 可以安装需要的软件

```
$ sudo docker exec -it smc bash
```

查看 smc 的日志信息, 可以看看container 的相关运行信息, 及时发现错误
```
sudo docker logs smc
```
### 自己动手配置

## 课程
每个被邀请加入课程的学生, SageMathCloud 都会在他的主目录下创建一个项目,
老师和助教都会自动成为这个项目的合作者.

学生的课程项目将会占用他自己的配额, 如硬盘存储, 网络访问等等.

布置任务

## 帮助链接

https://github.com/mikecroucher/SMC_tutorial#sagemathcloud
