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
```

### Memcached

Memcached directory: */data/apps/memcached*  
Memcached configuration file: */data/apps/memcached/.env*  

### Docker

Docker root directory: */var/lib/docker*  
Docker image directory: */var/lib/docker/image*   
Docker daemon.json: please create it when you need and save to to the directory */etc/docker*   

## Ports

These Ports is need when use Memcached, refer to [Safe Group Setting on Cloud Console](https://support.websoft9.com/docs/faq/tech-instance.html)

| Name | Number | Use |  Necessity |
| --- | --- | --- | --- |
| Memcached | 11211 | Remote connect Memcached | Optional |

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
docker inspect  memcached | grep com.docker.compose.version

# Docker version
docker -v
```