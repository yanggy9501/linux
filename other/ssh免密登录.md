# SSH 无密登录

## 1）ssh连接

（1）基本语法

```shell
ssh ip地址
ssh 用户@ip
```

（2）如果出现如下内容

* Are you sure you want to continue connecting (yes/no)? 

  输入yes

  输入密码

（3）退出登录远程

```shell
exit
```

## 2）无密登录

**无密钥配置原理**



**(1) 、生成公钥私钥**

```shell
ssh-keygen -t rsa
#或
ssh-keygen
```

然后三次回车，就会生成两个文件 id_rsa（私钥）、id_rsa.pub（公钥）



**（2）将公钥拷贝到要免密登录的目标机器上**

```shell
ssh-copy-id host
```

补充: .ssh目录下
