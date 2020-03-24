## Linux操作

![image-20200323182920738](C:\Users\dht24\AppData\Roaming\Typora\typora-user-images\image-20200323182920738.png)

终端文件颜色含义：

- 白色：普通文件
- 深蓝色：目录
- 绿色：可执行文件
- 红色：压缩文件
- 浅蓝色：链接文件
- 黄色：设备文件

常用命令：

- pwd:  显式当前路径
- mkdir 【目录名】： 创建文件夹
- mv [目录名称] [新目录名称] ：修改目录名称
- mv [目录名称] [目录的新位置] ：剪切
- cp -r [目录名称] [目录拷贝的目标位置] ：复制，-r代表递归拷贝
- rm -rf 目录： 递归删除

文件操作命令：

- touch [文件名称] ： 创建空文件
- cat/more/less/tail  [文件] ： 查看
- vim [文件] ：改，按i进入编辑模式，编辑完成后，按esc退出进入底行模式，:wq保存（:q!不保存）
- rm -rf 文件：删除文件

压缩文件命令：

- 打包并压缩后的文件后缀名为.tar.gz，tar -zcvf  [压缩后的文件名] [压缩的文件]，tar为打包，只有tar，打开后是散着的
- z: 调用gzip命令压缩， c:打包文件 ， v:显式运行过程 ，f:指定文件名
- tar [-xvf] 压缩文件：解压到当前目录，x代表解压
- tar [-xvf] 压缩文件 -C 指定目录：解压到指定目录

权限命令：

![image-20200323202154409](C:\Users\dht24\AppData\Roaming\Typora\typora-user-images\image-20200323202154409.png)

r:4  w:2  x:1

- chmod u=rwx,g=rw,o=r aaa.txt  :   修改权限
- chmod 764 aaa.txt:修改权限
- chgrp [-R] users install.log : 将install.log变为users用户组
- chown [-R] dang install.log ： 将install.log变为dang用户所有



查找

- rpm -qa | grep ×××：查找
- rpm -i 文件名：安装
- rpm -e 文件名：卸载



加载配置文件 source /etc/profile



mysql开放3306端口，并永久保存（Linux默认只开放22口）,tomcat就是开8080端口

/sbin/iptables -I INPUT -p tcp --dport 3306 -j ACCEPT

/etc/rc.d/init.d/iptables save ---将修改永久保存到防火墙中