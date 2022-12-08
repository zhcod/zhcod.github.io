---
layout: default
title: 代理
parent: WSL
---

    #!/bin/sh
    # 获取wsl2 ip地址
    hostip=$(cat /etc/resolv.conf | grep nameserver | awk '{ print $2 }')
    # 设置v2ray的IP（准备工作第二步）
    port=10811
    PROXY_HTTP="http://${hostip}:${port}"

    export http_proxy="${PROXY_HTTP}"
    export HTTP_PROXY="${PROXY_HTTP}"

    export https_proxy="${PROXY_HTTP}"
    export HTTPS_proxy="${PROXY_HTTP}"
    
