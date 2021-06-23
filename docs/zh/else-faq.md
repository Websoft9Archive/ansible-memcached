# FAQ

#### 什么是 Memcached 客户端？

Memcached 客户端是用于与 Memcached-Server 进行通信的程序，Memcached 是通过 Telnet 来运行客户端命令的。

#### Memcached 需要密码才能登录吗？

无需设置密码验证

#### 是否有可视化的数据库管理工具？

有，内置 Memcached-admin，访问地址：*http://服务器公网IP:9090*

#### 如何修改Memcached-admin 控制台密码？

运行下面的命令即可：  
```
htpasswd -b /etc/nginx/.htpasswd admin new_password
```

#### Memcached 服务端怎么配置？

参考 [命令与配置](/zh/solution-cli.md)

#### 部署和安装有什么区别？

部署是将一序列软件按照不同顺序，先后安装并配置到服务器的过程，是一个复杂的系统工程。  
安装是将单一的软件拷贝到服务器之后，启动安装向导完成初始化配置的过程。  
安装相对于部署来说更简单一些。 

#### 云平台是什么意思？

云平台指提供云计算服务的平台厂家，例如：Azure,AWS,阿里云,华为云,腾讯云等

#### 实例，云服务器，虚拟机，ECS，EC2，CVM，VM有什么区别？

没有区别，只是不同厂家所采用的专业术语，实际上都是云服务器