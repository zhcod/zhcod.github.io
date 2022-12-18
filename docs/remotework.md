---
layout: default
title: 远程办公指南
nav_order: 7
---

# 远程办公指南

思路：通过vscode的远程功能，可以实现接近本地代码编程编译运行的体验。  
由于没有公网ip，所以要通过vpn连接到校内网，再连接办公室主机。

## 1. 远端linux主机
~~~bash
# 先卸载原有的 ssh
sudo apt remove openssh-server
# 重新安装新的 ssh
sudo apt install openssh-server
# 开启ssh服务
sudo service ssh start
# 设置ssh服务开机自动启动
sudo systemctl enable ssh
~~~
## 2. 本地主机
~~~bash
# 生成密钥
ssh-keygen
~~~
在主机用户目录下会生成.ssh文件夹，里面的id_rsa是私钥，id_rsa.pub是公钥。  
我们只需把公钥里的内容粘贴到远程主机的.ssh文件夹里
（windows是c:\Users\用户名\ .ssh。linux是在~/.ssh ，没有的手动新建一个），
并命名为authorized_keys(不带任何后缀)。就行啦！
