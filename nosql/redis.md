# Deepin安装Redis

## 安装  
```
sudo apt-get install redis-server  
```

安装完成后，Redis服务器会自动启动，我们检查Redis服务器程序


## 检查Redis服务器系统进程  
```
ps -aux|grep redis  
```

## 查看redis端口状态  
```
netstat -nlt|grep 6379  
```

## 其他命令  

* 停用: 
```
/etc/init.d/redis-server stop
```  
* 启动: 
```
/etc/init.d/redis-server start 
``` 
* 重启: 
```
/etc/init.d/redis-server restart
```

# 安装redis-desktop-manager


官网地址：

https://snapcraft.io/redis-desktop-manager

https://snapcraft.io/install/redis-desktop-manager/debian

```
sudo apt update
sudo apt install snapd
```

```
sudo snap install redis-desktop-manager
```
切换到

/var/lib/snapd/snaps

找到

redis-desktop-manager_405.snap

```
snap install --dangerous redis-desktop-manager_405.snap
```