
1. 首先确定已经正确安装了MySQL数据库
2. 修改MySQL数据库的配置文件

输入命令：

```
sudo vi /etc/mysql/mysql.conf.d/mysqlld.cnf
```

3. 进入MySQL配置文件

按字母a键进入编辑模式，将bind-address的值修改为0.0.0.0，如图：

按Esc键退出编辑模式后，同时按住Shift键和：；键，左下角会出现一个冒号，输入wq,回车保存退出。

3.使用root用户登录MySQL数据库

打开终端，输入命令：mysql -u root -p

回车后看到Enter password:后，输入root用户密码。

4.创建用户用于远程连接

输入命令：
```
GRANT ALL PRIVILEGES ON *.* TO 'username'@'%' IDENTIFIED BY 'userpassword' WITH GRANT OPTION;
```

把username和userpassword改成自己的用户名和密码。

\*.*代表的所有数据库的所有表，第一个*指的是数据库名，第二个*指的是表名username：表示用户名；userpassword：表示密码；'%':表示所有的IP都可以访问。

5.刷新权限信息

输入命令：
```
FLUSH PRIVILEGES;
```

如果还连不上，可以重启一下系统。

备注：我的网络环境只限于局域网。