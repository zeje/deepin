deepin没有ll命令解决

ll命令其实是 ls -l命令的别名,在deepin中这个配置被注释掉了,使用下面的命令编辑配置文件打开即可

```
sudo vim ~/.bashrc
```
将alias ll=’ls -l’前的注释打开,然后source ~/.bashrc刷新一下即可