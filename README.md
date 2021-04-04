# ubuntu_mysql_install
ubuntu系统mysql的安装与配置 
---

安装
---  
ubuntu默认自带mysql包，更新apt软件包并安装即可。
```
#更新包
sudo apt-get update
#安装包
sudo apt-get install mysql-server
```
注意区分mysql的client和server。

配置
---
初始化指令
`sudo mysql_secure_installation`
详细配置
```
#1密码配置插件 规定了密码必要格式
VALIDATE PASSWORD PLUGIN can be used to test passwords...
Press y|Y for Yes, any other key for No: N （关闭）

#2
Please set the password for root here...
New password: (输入密码)
Re-enter new password: (重复输入)

#3
By default, a MySQL installation has an anonymous user,
allowing anyone to log into MySQL without having to have
a user account created for them...
Remove anonymous users? (Press y|Y for Yes, any other key for No) : N 

#4
Normally, root should only be allowed to connect from
'localhost'. This ensures that someone cannot guess at
the root password from the network...
Disallow root login remotely? (Press y|Y for Yes, any other key for No) : N 

#5
By default, MySQL comes with a database named 'test' that
anyone can access...
Remove test database and access to it? (Press y|Y for Yes, any other key for No) : N 

#6
Reloading the privilege tables will ensure that all changes
made so far will take effect immediately.
Reload privilege tables now? (Press y|Y for Yes, any other key for No) : Y 
``` 

mysql运行检查
---
输入指令 
`systemctl status mysql.service` 
如下显示则安装成功
![mysqlcheck](https://user-images.githubusercontent.com/75117698/113504539-5da3fe80-956b-11eb-9634-fafe31574ace.png)
