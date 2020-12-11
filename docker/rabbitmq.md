# RabbitMq

> 官网：https://www.rabbitmq.com/getstarted.html

## 前置条件：

已经安装好docker

## 用docker部署RabbitMQ环境

1. 查找镜像（有2种方式）

* 登录rabbitmq官网找到docker镜像，选择想要的镜像的tag

https://www.rabbitmq.com/download.html

https://hub.docker.com/_/rabbitmq

* 直接用docker search 搜索，默认下载标签为latest的镜像（无法打开web管理页面）

2. 通过指令拉取镜像　   

下载镜像（有时候网络问题超时，多尝试几次即可。我这里选择的是可以访问web管理界面的tag）

```
sudo docker pull rabbitmq:management
```     
3. 创建容器并运行

（15672是管理界面的端口，5672是服务的端口。这里顺便将管理系统的用户名和密码设置为admin admin）

```
docker run -dit --name zejeRabbitMq -e RABBITMQ_DEFAULT_USER=admin -e RABBITMQ_DEFAULT_PASS=admin -p 15672:15672 -p 5672:5672 rabbitmq:management
```
4. 打开浏览器

```
http://localhost:15672
```
