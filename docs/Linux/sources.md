---
layout: default
titile: 换哈工大源
parent: Linux
---
```bash
#!/bin/bash
# 备份源
sudo mv -f /etc/apt/sources.list /etc/apt/sources.list.backup
sudo bash -c "cat>/etc/apt/sources.list"<<EOF
# 默认注释了源码镜像以提高 apt update 速度，如有需要可自行取消注释
deb http://mirrors.hit.edu.cn/ubuntu/ jammy main restricted universe multiverse
# deb-src http://mirrors.hit.edu.cn/ubuntu/ jammy main restricted universe multiverse
deb http://mirrors.hit.edu.cn/ubuntu/ jammy-updates main restricted universe multiverse
# deb-src http://mirrors.hit.edu.cn/ubuntu/ jammy-updates main restricted universe multiverse
deb http://mirrors.hit.edu.cn/ubuntu/ jammy-backports main restricted universe multiverse
# deb-src http://mirrors.hit.edu.cn/ubuntu/ jammy-backports main restricted universe multiverse
deb http://mirrors.hit.edu.cn/ubuntu/ jammy-security main restricted universe multiverse
# deb-src http://mirrors.hit.edu.cn/ubuntu/ jammy-security main restricted universe multiverse
# 预发布软件源，不建议启用
# deb http://mirrors.hit.edu.cn/ubuntu/ jammy-proposed main restricted universe multiverse
# deb-src http://mirrors.hit.edu.cn/ubuntu/ jammy-proposed main restricted universe multiverse
EOF
```
