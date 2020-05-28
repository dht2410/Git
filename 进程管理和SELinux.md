将命令丢到后台执行： 在正常命令后加 & ，控制台打印信息的可以重定向 >

暂停执行：Ctrl+Z

查看后台工作状态：jobs  [-lrs]  -l是list，-r是run的，-s是stop的

将后台工作拿到前台处理：fg %jobnumber

让工作在后台的状态下变成运行中：bg

结束进程：kill  -signal  %jobnumber    或者是  kill  -signal  PID

signal可为

- -1：重新读取一次参数的配置文件
- -2：同ctrl+C
- -9：强制删除一个工作
- -15：以正常方式终止一项工作



### 查看进程

ps -l：和bash有关的进程

ps aux：系统此时的进程情况

top：查看实时进程情况

### 进程优先级

PRI显式的是进程优先级，越小优先级越高

PRI（new）=PRI（old）+NI

### 资源查看

free：系统内存查看  -b|-k|-m|-g为单位

netstat : 跟踪网络    -tlnp  查看监听的端口

