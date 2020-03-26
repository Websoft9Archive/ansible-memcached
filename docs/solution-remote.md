# Memcached remote connection

When you want to use local terminal to connect Memcached-Sever,you need to configure remote connection at first.

There need at least two step for this configuration of Memcached:

## Enable TCP:6379 port

Check your **[Inbound of Security Group Rule](https://support.websoft9.com/docs/faq/tech-instance.html)** of Cloud Console to ensure the **TCP:6379** is allowed


## Enable connection from all the network 

You should check your [Memcached configuration file](/stack-components.md#redis) the following segment

```
# By default Memcached listens for connections from all the network interfaces
# available on the server. It is possible to listen to just one or multiple
# interfaces using the "bind" configuration directive, followed by one or
# more IP addresses.
#
# Examples:
#
# bind 192.168.1.100 10.0.0.1
# bind 127.0.0.1
```