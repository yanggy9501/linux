# vmware网络



# centos网络设置

**配置文件**

```shel
# 不同系统/主机配置文件不一样
vim /etc/sysconfig/network-scripts/ifcfg-ens33
```

* 内容(去掉中文)

```
TYPE="Ethernet"
PROXY_METHOD="none"
BROWSER_ONLY="no"
BOOTPROTO="static" # 静态IP地址
DEFROUTE="yes"
IPV4_FAILURE_FATAL="no"
IPV6INIT="yes"
IPV6_AUTOCONF="yes"
IPV6_DEFROUTE="yes"
IPV6_FAILURE_FATAL="no"
IPV6_ADDR_GEN_MODE="stable-privacy"
NAME="ens33"
UUID="8fe73ec1-2fcf-4a5f-bc3e-77263095eed1"
DEVICE="ens33"
ONBOOT="yes"
IPADDR=192.168.134.132 # IP地址ens33，必须和vmware保持同一个网段
PREFIX=24 # 子网个数
GATEWAY=192.168.134.2 # 网关
DNS1=192.168.134.2 # DNS

```

