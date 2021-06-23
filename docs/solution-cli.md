# Configure and command

You can configure Memcached container (Server) and use Telnet client at this deployment solution  

## Commandline Arguments

If you want to configure Memcached Server, you should configure [Commandline Arguments](https://github.com/memcached/memcached/wiki/ConfiguringServer#commandline-arguments) by like below steps:  

1. Use SFTP to connect Server and edit */data/apps/memcached/docker-compose.yml* file, add more items for **command** parameter
    ```
    version: '3.8'
    services:
    memcached:
        image: memcached:${APP_VERSION}
        container_name: ${APP_CONTAINER_NAME}
        restart: always
        command:
        - '-m 800'
    ```

2. Recreate containers
   ```
   cd /data/apps/memcached
   sudo docker-compose up -d
   ```

## Telnet client

Memcached does not provide specific client. However, standard tools like telnet are enough to test container. Under Linux it is possible to connect by CLI command. We can invoke telnet from host machine, to connect to running Memcached server

1. Use SSH to connect Sever and use Telnet connect Memcached
```
telnet 127.0.0.1 11211
Trying 127.0.0.1...
Connected to 127.0.0.1.
Escape character is '^]'.
```

2. Then, input `stats` command to list all configuration of Memcached

More details please refer to docs: [Memcached Commands](https://github.com/memcached/memcached/wiki/Commands)