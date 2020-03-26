# 参数

Memcached 预装包包含 Memcached 运行所需一序列支撑软件（简称为“组件”），下面列出主要组件名称、安装路径、配置文件地址、端口、版本等重要的信息。

## 路径

### Memcached

Memcached安装目录: */usr/share/memcached*
Memcached配置文件目录：*/etc/memcached.conf*
Memcached日志文件目录：*/var/log/memcached.log*

### 其他

暂无辅助工具

## 端口号

下面是您在使用本镜像过程中，需要用到的端口号，请通过 [云控制台安全组](https://support.websoft9.com/docs/faq/zh/tech-instance.html)进行设置

| 名称 | 端口号 | 用途 |  必要性 |
| --- | --- | --- | --- |
| Memcached | 11211 | 远程访问 Memcached | 可选 |

运行命令下列命令查看所有端口占用情况
```
netstat -anopt | grep LISTEN

tcp        0      0 0.0.0.0:22              0.0.0.0:*               LISTEN      5337/sshd            off (0.00/0/0)
tcp        0      0 0.0.0.0:11211           0.0.0.0:*               LISTEN      651/memcached        off (0.00/0/0)
tcp6       0      0 :::22                   :::*                    LISTEN      5337/sshd            off (0.00/0/0)
tcp6       0      0 :::11211                :::*                    LISTEN      651/memcached        off (0.00/0/0)
```

## 版本号

组件版本号可以通过云市场商品页面查看。但部署到您的服务器之后，组件会自动进行更新导致版本号有一定的变化，故精准的版本号请通过在服务器上运行命令查看：

```shell
# Linux Version
lsb_release -a

# Memcached version
yum info memcached
```