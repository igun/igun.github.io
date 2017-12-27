---
categories:
  - Sysadmin
tags:
  - linux
  - centos
  - quickie
title: "Setup ifconfig pada centos 7"
slug: "centos 7 ifconfig"
date: "2017-12-28T06:13:48+07:00"
draft: true
---

Untuk melakukan setting network pada OS Centos 7, edit file pada lokasi berikut:

```
# vi /etc/sysconfig/network-scripts/ifcfg-eth0
```

Dengan content file sebagai berikut:

```
TYPE="Ethernet"
BOOTPROTO="static"
NAME="eth0"
DEVICE="eth0"
ONBOOT="yes"
IPADDR=192.168.0.2
NETMASK=255.255.255.0
GATEWAY=192.168.0.1
DNS1=8.8.8.8
DNS2=8.8.4.4
```

Untuk interface lain, nama file nya adalah **ifcfg-interface**. ex: **ifcfg-eth1**, **ifcfg-eth2**, dll.
