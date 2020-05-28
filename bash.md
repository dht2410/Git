- env    展示环境变量
- echo $[变量] ：显示变量
- read [-pt] 变量名：读键盘输入，-p后跟提示符，-t后跟秒数
- declare [-aixr] 变量名：声明变量类型。-a数组，-i整型，-x变成环境变量

命令执行顺序：

- 先找alias中的
- 再找内置的
- 最后从环境变量$PATH中按顺序找

登录信息在/etc/issue中

开机读取全局配置信息/etc/profile，调用读取用户配置信息~/.bash_profile，链式调用，最后开启bash

source [配置文件名] 或 . [配置文件名]   将配置信息读进shell环境

### 重定向redirect

- ls > ./a.txt	屏幕打印的信息写到文件
- ls >> ./a.txt     屏幕打印的信息写到文件末尾
- find /home -name .bashrc >list_right 2> list_error    正确信息写到right，错误信息写到error. 输出正确返回1，输出错误返回2
- cat > catfile < ~/.bashrc    把~/.bashrc内容输入到catfile中

### pipe

|前的输出作为|后的输入

|后面接的第一个数据必须是命令，且能够接收standard output

选取命令：

- cut
- grep

排序命令：

- sort
- wc
- uniq

双向重定向：

- tee