# 初始化验证

在云服务器上部署 Memcached 预装包之后，请参考下面的步骤快速入门。

## 准备

1. 在云控制台获取您的 **服务器公网IP地址** 
2. 在云控制台安全组中，检查 **Inbound（入）规则** 下的 **TCP:6379** 端口是否开启
3. 若想用域名访问 Memcached，请先到 **域名控制台** 完成一个域名解析

## Memcached 检验

1. 通过 SSH 工具连接 Memcached服务器

2. 运行 telnet 命令，连接 Memcached
   ```
   telnet 127.0.0.1 11211
   Trying 127.0.0.1...
   Connected to 127.0.0.1.
   Escape character is '^]'.
   ```
3. 连接成功，系统进入 Memcached 命令行输入状态，输入命令 `stats`
   ```
   STAT pid 651
   STAT uptime 891
   STAT time 1585225158
   STAT version 1.4.15
   STAT libevent 2.0.21-stable
   STAT pointer_size 64
   STAT rusage_user 0.005846
   STAT rusage_system 0.017539
   STAT curr_connections 10
   STAT total_connections 12
   STAT connection_structures 11
   STAT reserved_fds 20
   STAT cmd_get 0
   STAT cmd_set 0
   STAT cmd_flush 0
   STAT cmd_touch 0
   STAT get_hits 0
   STAT get_misses 0
   STAT delete_misses 0
   STAT delete_hits 0
   STAT incr_misses 0
   STAT incr_hits 0
   STAT decr_misses 0
   STAT decr_hits 0
   STAT cas_misses 0
   STAT cas_hits 0
   STAT cas_badval 0
   STAT touch_hits 0
   STAT touch_misses 0
   STAT auth_cmds 0
   STAT auth_errors 0
   STAT bytes_read 52
   STAT bytes_written 21
   STAT limit_maxbytes 67108864
   STAT accepting_conns 1
   STAT listen_disabled_num 0
   STAT threads 4
   STAT conn_yields 0
   STAT hash_power_level 16
   STAT hash_bytes 524288
   STAT hash_is_expanding 0
   STAT bytes 0
   STAT curr_items 0
   STAT total_items 0
   STAT expired_unfetched 0
   STAT evicted_unfetched 0
   STAT evictions 0
   STAT reclaimed 0
   END

   ```
4. 输入命令 `quit` 退出系统

> 需要了解更多Memcached的使用，请参考：[Memcached Wiki](https://github.com/memcached/memcached/wiki)

## 常见问题

#### Telnet 无法连接 Memcached？

请检查服务器是否已安装telnet，同时查看11211端口是否开启

#### 本部署是否提供Web版的可视化管理工具？

没有，我们暂时还没有发现稳定可靠的 Web-GUI for Memcached
