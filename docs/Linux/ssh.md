---
layout: default
title: ssh
parent: Linux
---

1. ssh基础命令

        ssh user@remote -p port 

其中user是用户名  
remote是服务器地址  
port是端口，默认值为22

2. 生成密钥  

        ssh-keygen  
生成的公钥放在了~/.ssh/id_rsa.pub, 私钥放在了~/.ssh/id_rsa。

3. known_hosts

存储了服务器的公钥