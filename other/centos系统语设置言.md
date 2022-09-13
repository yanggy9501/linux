# 改 centos 系统语言

* 1、查看系统当前语言包

  ```shell
  locale
  ```

* 2，查看系统拥有语言包

```linux
locale -a
```

（zh_CN.UTF-8是简体中文，如果没有zh_CN.UTF-8,就安装语言包，如果存在可以直接设置)

* 3、安装简体中文语言包

  ```linux
  yum install kde-l10n-Chinese
  ```

* 4，设置为中文

  * 临时修改，重启服务器之后就会还原之前的设置

    ```linux
    LANG="zh_CN.UTF-8"    #修改为中文
    
    LANG="en_US.UTF-8"    #修改为英文
    ```

  * 永久修改就要把配置写入文件里面。

    方法（一）

    vi /etc/locale.conf ##加下面内容到第一行，设置中文.UTF8

    方法（二）

    localectl set-locale.UTF

