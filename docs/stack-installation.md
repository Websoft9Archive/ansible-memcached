# Initial check

If you have completed the Memcached deployment on Cloud Platform, the following steps is for you to start use it quikly

## Preparation

1. Get the **Internet IP** on your Cloud Platform
2. Check your **[Inbound of Security Group Rule](https://support.websoft9.com/docs/faq/tech-instance.html)** of Cloud Console to ensure the **TCP:6379** is allowed
3. Make a domain resolution on your DNS Console if you want to use domain for Memcached

## Memcached check

1. Use **SSH** tool to connect Memcached Server

2. Run the command `sudo systemctl status redis` to check the service state of Memcached
   ```
   ubuntu@redis:~$ sudo systemctl status redis 
   redis.service - redis
   Loaded: loaded (/lib/systemd/system/redis.service; enabled; vendor preset: en
   Active: active (running) since Mon 2020-02-03 10:03:09 UTC; 2h 27min ago
   Process: 31972 ExecStart=/usr/local/bin/redis-server /etc/redis/redis.conf (co
   Main PID: 31973 (redis-server)
   ```
3. Run the command `sudo systemctl status redis` to check the version of Memcached
   ```
   ubuntu@redis:~$ sudo redis-server -v
   Memcached server v=2.8.24 sha=00000000:0 malloc=jemalloc-3.6.0 bits=64 build=ba7fac81f854c786
   ```
4. Go to **Memcached CLI** to test it
   ```
   ubuntu@redis:~$ redis-cli
   127.0.0.1:6379>
   ```
> More useful Memcached guide, please refer to [Memcached Documentation](https://redis.io/documentation)

## Q&A 

#### Can't connect Memcached from remote?

1. Check your **[Inbound of Security Group Rule](https://support.websoft9.com/docs/faq/tech-instance.html)** of Cloud Console to ensure the **TCP:6379** is allowed
2. Check your **Memcached configuration file** that Memcached allowed from Internet

#### Is there any Web-GUI tool for Memcached in this deployment solution?

No, you can refer to [Memcached GUI](/solution-gui.md) chapter of this docs