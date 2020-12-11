# docker 设置国内镜像源

创建或修改 /etc/docker/daemon.json 文件，修改为如下形式

```
# vi /etc/docker/daemon.json
```

```
{   
     "registry-mirrors": ["http://hub-mirror.c.163.com"]
}
```

```
systemctl restart docker.service
```

# Docker 国内仓库和镜像

> 由于网络原因，我们在pull Image 的时候，从Docker Hub上下载会很慢。。。所以，国内的Docker爱好者们就添加了一些国内的镜像（mirror）,方便大家使用。

## 1. 国内 Docker 仓库

* [阿里云](https://dev.aliyun.com/search.html)
* [网易云](https://c.163yun.com/hub#/m/home/)
* [时速云](https://hub.tenxcloud.com/)
* [DaoCloud](https://hub.daocloud.io/)

## 2. 国外 Docker 仓库

* [Docker Hub](https://hub.docker.com/)
* [Quay](https://quay.io/)

## 3. 配置 Docker 镜像加速

### 3-1. 国内加速站点

* [https://registry.docker-cn.com](https://registry.docker-cn.com/)
* [http://hub-mirror.c.163.com](http://hub-mirror.c.163.com/)
* [https://3laho3y3.mirror.aliyuncs.com](https://3laho3y3.mirror.aliyuncs.com/)
* [http://f1361db2.m.daocloud.io](http://f1361db2.m.daocloud.io/)
* [https://mirror.ccs.tencentyun.com](https://mirror.ccs.tencentyun.com/)

### 3-2. 使用命令来配置加速站点

```
mkdir -p /etc/docker
sudo tee /etc/docker/daemon.json <<-'EOF'
{
  "registry-mirrors": ["<your accelerate address>"]
}
```

### 3-3. 使用脚本来配置加速站点

该脚本可以将`--registry-mirror`加入到你的`Docker`配置文件`/etc/docker/daemon.json`中。适用于`Ubuntu14.04、Debian、CentOS6 、CentOS7、Fedora、Arch Linux、openSUSE Leap 42.1`，其他版本可能有细微不同。更多详情请访问文档。

```language-shell
curl -sSL https://raw.githubusercontent.com/wss434631143/xiaoshujiang/master/articles/Docker/shell/set_mirror.sh | sh -s <your accelerate address>
```

### 3-4. 通过修改启动脚本配置加速站点

```
# 直接修改 /usr/lib/systemd/system/docker.service 启动脚本
vim /usr/lib/systemd/system/docker.service 
# 在dockerd后面加参数
ExecStart=/usr/bin/dockerd --registry-mirror=<your accelerate address>
```

### 以上操作后重启一下`Docker`

```language-shell
sudo systemctl daemon-reload
sudo systemctl restart docker
```