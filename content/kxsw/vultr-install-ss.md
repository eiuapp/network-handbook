---
date: 2019-01-08T21:07:13+01:00
title: "vultr(vps)搭建ss"
weight: 11
keywords:
- 学习笔记
- vultr
description : "vultr"
---


使用vultr(vps)搭建ss并开启BBR快速上网教程 超简单10分钟搞定

https://wistbean.github.io/vultr-vps-bbr-ss.html 

## 安装shell script

```bash
yum install wget
wget --no-check-certificate -O shadowsocks.sh https://raw.githubusercontent.com/teddysun/shadowsocks_install/master/shadowsocks.sh
chmod +x shadowsocks.sh
./shadowsocks.sh 2>&1 | tee shadowsocks.log
```

## check ip-port

- http://coolaf.com/tool/port

### no acceptable C compiler found in $PATH when installing 

 参考[这里](https://stackoverflow.com/questions/19816275/no-acceptable-c-compiler-found-in-path-when-installing-python)

```bash
yum groupinstall "Development Tools"
```

### which python

```bash
yum install python2
ln -s /usr/bin/python2 /usr/bin/python
```

### close firewalld

```bash
systemctl status firewalld.service
systemctl stop firewalld.service
```
