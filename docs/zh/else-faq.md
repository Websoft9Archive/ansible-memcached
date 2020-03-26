# FAQ

#### 什么是Memcached客户端？

Memcached 客户端是用于与Memcached-Server进行通信的程序，例如：redis-cli 就是典型的客户端工具

#### Memcached Labs 与 Memcached 有什么关系？

[Memcached Labs](https://redislabs.com/) 是 Memcached 的母公司，即 Memcached 是 Memcached Labs 公司旗下的产品。

#### Memcached需要密码才能登录吗？

可以无需设置密码验证

#### Memcached 支持哪些数据结构？

Memcached不是简单的键值存储，它实际上是一个数据结构服务器，支持不同类型的值。包括：二进制字符串、列表、集合、哈希、位图、HyperLogLogs、流等

#### 是否有可视化的数据库管理工具？

部分Memcached镜像已经安装 MemcachedInsight 这个可视化管理工具，如果没有安装，您可以自行安装。

#### 是否可以修改Memcached的源码路径？

不可以修改

#### 部署和安装有什么区别？

部署是将一序列软件按照不同顺序，先后安装并配置到服务器的过程，是一个复杂的系统工程。  
安装是将单一的软件拷贝到服务器之后，启动安装向导完成初始化配置的过程。  
安装相对于部署来说更简单一些。 

#### 云平台是什么意思？

云平台指提供云计算服务的平台厂家，例如：Azure,AWS,阿里云,华为云,腾讯云等

#### 实例，云服务器，虚拟机，ECS，EC2，CVM，VM有什么区别？

没有区别，只是不同厂家所采用的专业术语，实际上都是云服务器