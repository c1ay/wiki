---
title: "普通用户，加入docker用户组，去掉sudo"
date: 2017-03-31 15:22
---

操作顺序:
1. `sudo cat /etc/group | grep docker`
2. 如果不存在`docker`组，可以添加`sudo groupadd docker`
3. 添加当前用户到docker组，`sudo gpasswd -a ${USER} docker`
4. 重启docker服务,`sudo systemctl restart docker`
5. 如果权限不够，`sudo chmod a+rw /var/run/docker.sock`

