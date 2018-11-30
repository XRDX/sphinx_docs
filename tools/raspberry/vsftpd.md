## 在树莓派安装vsftpd服务器



### vsftpd

vsftpd是开源的轻量级的常用ftp服务器．



1,安装vsftpd服务器 (约400KB)
sudo apt-get install vsftpd



2,启动ftp服务
sudo service vsftpd start



3,编辑vsftdp的配置文件

sudo nano /etc/vsftpd.conf



找到以下行，定义一下
anonymous_enable=NO  

表示：不允许匿名访问

local_enable=YES   

设定本地用户可以访问。

write_enable=YES

设定可以进行写操作



local_umask=022

设定上传后文件的权限掩码。



存盘退出



4, 重启vsftpd服务
sudo service vsftpd restart



5, 测试一下, OK

通过ftp连接树莓派系统，以用户名pi登录，密码是raspberry

ftp的根目录是/home/pi，即pi用户的HOME目录

可上传或下载文件了