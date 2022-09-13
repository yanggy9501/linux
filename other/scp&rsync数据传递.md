# 1，scp（secure copy）安全拷贝

（1）scp定义

scp可以实现服务器之间的数据拷贝

（2） 基本语法

```shell
scp 		-r		 $pdir/$fname 		$suer@$host:$pdir/$fname
命令			递归	要拷贝的文件路径/名称		目的地用户@主机：目的地路径/名称

scp -r /opt/jdk.18 root@192.168.134.129:/usr/local/src
```

案例

* A主机拷贝B主机
* B主机拷贝A主机
* C主机实现A拷贝B



# 2，rsync远程同步工具

​		rsync 主要用于备份和镜像。具有速度快，避免复制相同内容和支持符号链接的优点。

**安装**

```shell
yum install rsync -y
```

(1)、基本语法

```shell
rsync 	-av 	$pdir/$fname		$user@$host:$pdir/$fname
命令		参数	要拷贝的文件路径/名称		目的地用户@主机：目的地路径/名称

-a：归档拷贝
-v：显示复制过程
```

案例

```shell
rsync -av hadoop-3.1.3/ root@192.168.134.129:/opt/module/hadoop-3.1.3/
```



# 3，xsync自定义分发脚本
