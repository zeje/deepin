# 使用deepin系统办公开发运维

1. 关于深度

deepin是基于debian开发的国产桌面操作系统。

选择deepin，是基于国产化，能办公，能开发，能运维的考虑。
它没有win10那样花里胡哨的用不上的功能，系统体积小，节省空间。不需要考虑病毒和系统垃圾。系统监控通过轻量级开源工具实施。

* 能办公

    deepin的高颜值，设置成本低。

    具备两种模式设置，显然时候模仿了Windows和Mac风格。

    常用软件:
    * 谷歌浏览器，搜狗输入法，微信，WPS
    * 坚果云，百度云
    * 网易云音乐，
    * 深度影音，深度编辑器
    * 其他工具：utools（使用utools有很多插件可以使用，包括一个音乐插件，能够检索到很多平台的音乐）
    * 能够与Windows系统共享文件
    * 支持移动设备(优盘，硬盘)
    * 支持主流打印机
* 能开发
    * 编辑器
        * vim
        * vscode
    * 环境
        * bash,c,python2/3
        * go,java,php
        * mysql,redis
        * apache,nginx
* 能运维
    * 集群管理工具:ansible,pdsh等
    * 虚拟化环境:kvm,vmware-workstation
    * 容器环境:docker
    * 其他环境:ntpd,openldap,sshd,ftpd,nfs,samba

## deepin配置

* 做减法

    如果不需要就卸载掉，不能通过应用商店删除的，可以使用sudo apt-get autoremove卸载


* 快捷键
    
    快捷键意味着高效(和装逼)
    deepin支持一些类似Windows10上面的快捷键，降低用户学习和过度成本。比如：

    * win 启动器
    * win+e 打开文件管理器
    * win+l 锁屏
    * win+d 回到桌面
    * win+up 最大化
    * win+down 恢复

## 快捷键配置

微信快捷键配置。其实很简单，如果在撸代码的过程中，发现任务栏有微信通知，直接alt+w就可以打开微信。
截图快捷键。个人喜欢是会用ctrl+alt+z作为截图快捷键，可以在设置-键盘-快捷键进行重新设置。
截图带通知，如果不喜欢，就可以自定义快捷键，命令中添加不通知的参数。

浏览器打开。一般情况下 ，我喜欢在任务来只放浏览器和终端。可以设置全局快捷键win+1，打开谷歌浏览器；设置全局快捷键win+2打开终端。
2.3 个性化配置
启动器快捷方式

在启动器上有很多快捷方式，如果不喜欢，是可以删除的。但是不建议删除，因为有的时候会导致文件无法找到默认的程序。
默认防止在:/usr/share/applications

## 自带壁纸

通过命令的方式删除｀sudo atp-get autoremove deepin-wallpapers｀。

壁纸目录放置在:｀/usr/share/wallpapers/deepin｀

## 启动器图标

deepin的启动器图标如果不喜欢的话，也可以自己制作svg格式，进行替换。
系统图标放置在:/usr/share/icons。该目录下不同的目录是不同的主题