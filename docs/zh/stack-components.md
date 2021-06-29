---
sidebarDepth: 3
---

# 参数

Memcached 预装包包含 Memcached 运行所需一序列支撑软件（简称为“组件”），下面列出主要组件名称、安装路径、配置文件地址、端口、版本等重要的信息。

## 路径

```
CONTAINER ID   IMAGE                                 COMMAND                  CREATED             STATUS             PORTS                                           NAMES
5f7322ff5805   memcached:latest                      "docker-entrypoint.s…"   About an hour ago   Up About an hour   0.0.0.0:11211->11211/tcp, :::11211->11211/tcp   memcached
e4e671827a3e   hatamiarash7/memcached-admin:latest   "docker-php-entrypoi…"   4 minutes ago   Up 4 minutes   0.0.0.0:8080->80/tcp, :::8080->80/tcp           memcached-admin
```

### Memcached

Memcached 安装目录: */data/db/memcached*  
Memcached 配置文件：*/data/db/memcached/.env*  

### Memcached-admin

[Memcached-admin](https://github.com/hatamiarash7/Memcached-Admin) 是一个用于管理和监控 Memcached 的可视化工具  

Memcached 安装目录: */data/apps/memadmin*  
Memcached 配置文件：*/data/apps/memadmin/.env*  

### Nginx

Nginx 虚拟主机配置文件：*/etc/nginx/conf.d/default.conf*  
Nginx 主配置文件： */etc/nginx/nginx.conf*  
Nginx 日志文件： */var/log/nginx*  
Nginx 伪静态规则目录： */etc/nginx/conf.d/rewrite*  
Nginx 验证访问文件：*/etc/nginx/.htpasswd/htpasswd.conf*  

> 本部署方案中 Nginx 验证访问文件存储了 Memcached-admin 的账号密码

### Docker

Docker 根目录: */var/lib/docker*  
Docker 镜像目录: */var/lib/docker/image*   
Docker daemon.json 文件：默认没有创建，请到 */etc/docker* 目录下根据需要自行创建   

## 端口号

在云服务器中，通过 **[安全组设置](https://support.websoft9.com/docs/faq/zh/tech-instance.html)** 来控制（开启或关闭）端口是否可以被外部访问。 

通过命令`netstat -tunlp` 看查看相关端口，下面列出可能要用到的端口：


| 名称 | 端口号 | 用途 |  必要性 |
| --- | --- | --- | --- |
| Memcached | 11211 | 远程访问 Memcached | 可选 |
| Memcached-admin | 9090 | 通过 Nginx 远程访问 Memcached 可视化工具 | 可选 |


## 版本号

组件版本号可以通过云市场商品页面查看。但部署到您的服务器之后，组件会自动进行更新导致版本号有一定的变化，故精准的版本号请通过在服务器上运行命令查看：

```shell
# Check all components version
sudo cat /data/logs/install_version.txt

# Linux Version
lsb_release -a

# Memcached version
docker inspect  memcached | grep com.docker.compose.version

# Docker version
docker -v

# Nginx  Version
nginx -V
```