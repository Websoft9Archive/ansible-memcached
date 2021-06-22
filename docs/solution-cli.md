# Memcached Commands

Memcached does not provide specific client. However, standard tools like telnet are enough to test container. Under Linux it is possible to connect by CLI command. We can invoke telnet from host machine, to connect to running Memcached server

```
telnet 127.0.0.1 11211
```

More details please refer to docs: [Memcached Commands](https://github.com/memcached/memcached/wiki/Commands)