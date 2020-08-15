# 下载SDK

> https://www.oracle.com/java/technologies/javase/javase-jdk8-downloads.html

# rpm方式安装java

安装失败，不研究了

# 压缩包安装方式

* 下载`jdk-8u261-linux-x64.tar.gz`
* 目标目录`/home/caizz/Downloads`
* 解压缩至`/data/opt/jdk1.8.0_261`目录下

# 配置

sudo update-alternatives --install /usr/bin/java java  /data/opt/jdk1.8.0_261/bin/java 1000 
sudo update-alternatives --install /usr/bin/javac javac  /data/opt/jdk1.8.0_261/bin/javac 1000

其他方式都是坑人的

# 如上配置,可能IDE识别不了classpath


