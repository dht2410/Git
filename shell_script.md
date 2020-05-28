source执行一个shell script是在父进程中执行，变量保留

sh执行一个shell script是在子进程中执行，变量不保留

执行的文件可以任何命名，无需.sh扩展名

但java文件需要.java扩展名，不然无法编译



条件判断：

```shell
if [ 条件判断 ];then
	命令
fi
```

```shell
if [ 条件判断 ];then
	命令
elif [ 条件判断 ];then
	命令
fi
```

循环（loop）:

```shell
while [ condition ]
do
	程序
done
```

```shell
for var in con1,con2,con3
do
	程序
done
```

**调试**

sh -x sh01.sh      显示每一句执行的语句

