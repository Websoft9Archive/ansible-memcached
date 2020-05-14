# Initial check

If you have completed the Memcached deployment on Cloud Platform, the following steps is for you to start use it quikly

## Preparation

1. Get the **Internet IP** on your Cloud Platform
2. Check your **[Inbound of Security Group Rule](https://support.websoft9.com/docs/faq/tech-instance.html)** of Cloud Console to ensure the **TCP:11211** is allowed
3. Make a domain resolution on your DNS Console if you want to use domain for Memcached

## Memcached check

1. Use **SSH** tool to connect Memcached Server

2. Use the telnet to connect Memcached
   ```
   telnet 127.0.0.1 11211
   Trying 127.0.0.1...
   Connected to 127.0.0.1.
   Escape character is '^]'.
   ```
3. Run the command `stats` to show all Memcached STAT when connection successful
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
4. Run the command `quit` if you want to exist Memcached

> More useful Memcached guide, please refer to [Memcached Wiki](https://github.com/memcached/memcached/wiki)

## Q&A 

#### Can't connect Memcached by Telnet?

Please make sure you Telnet installed and port **11211** enabled

#### Is there any Web-GUI tool for Memcached in this deployment solution?
No