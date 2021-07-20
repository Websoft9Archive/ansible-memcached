---
sidebarDepth: 3
---

# Parameters

The Memcached deployment package contains a sequence of software (referred to as "components") required for Memcached to run. Below list the important information, the component name, installation directory path, configuration file path, port, version, etc.

## Path

This solution use Docker to deploy all service, you can run the command docker ps to list them

```
CONTAINER ID   IMAGE                                 COMMAND                  CREATED             STATUS             PORTS                                           NAMES
5f7322ff5805   memcached:latest                      "docker-entrypoint.s…"   About an hour ago   Up About an hour   0.0.0.0:11211->11211/tcp, :::11211->11211/tcp   memcached
e4e671827a3e   hatamiarash7/memcached-admin:latest   "docker-php-entrypoi…"   4 minutes ago   Up 4 minutes   0.0.0.0:8080->80/tcp, :::8080->80/tcp           memcached-admin
```

### Memcached

Memcached directory: */data/db/memcached*  
Memcached configuration file: */data/db/memcached/.env*  

### Memcached-admin

[Memcached-admin](https://github.com/hatamiarash7/Memcached-Admin) is a Web-based GUI tool for Memcached

Memcached directory: */data/apps/memcached-admin*  
Memcached configuration file: */data/apps/memcached-admin/.env*  

### Nginx

Nginx vhost configuration file: */etc/nginx/conf.d/default.conf*    
Nginx main configuration file: */etc/nginx/nginx.conf*   
Nginx logs file: */var/log/nginx*  
Nginx rewrite rules directory: */etc/nginx/conf.d/rewrite*  
Nginx htpasswd file: */etc/nginx/.htpasswd/htpasswd.conf* 

> Nginx htpasswd file have storage the username and password for Memcached-admin

### Docker

Docker root directory: */var/lib/docker*  
Docker image directory: */var/lib/docker/image*   
Docker daemon.json: please create it when you need and save to to the directory */etc/docker*   

## Ports

These Ports is need when use Memcached, refer to [Safe Group Setting on Cloud Console](https://support.websoft9.com/docs/faq/tech-instance.html)

| Name | Number | Use |  Necessity |
| --- | --- | --- | --- |
| TCP | 11211 | Remote connect Memcached | Optional |
| TCP | 9090 | HTTP to access Memcached-admin reverse proxy by Nginx | Optional |

## Version

Open or close ports by **[Security Group Setting](https://support.websoft9.com/docs/faq/tech-instance.html)** of your Cloud Server to decide whether the port can be accessed from Internet.  

You can run the cmd `netstat -tunlp` to check all related ports.  

The following are the ports you may use:

```shell
# Check all components version
sudo cat /data/logs/install_version.txt

# Linux Version
lsb_release -a

# Memcached version
docker inspect  memcached | grep MEMCACHED_VERSION

# Docker version
docker -v

# Nginx  Version
nginx -V
```
