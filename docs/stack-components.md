# Parameters

The Memcached deployment package contains a sequence software (referred to as "components") required for Memcached to run. The important information such as the component name, installation directory path, configuration file path, port, version, etc. are listed below.

## Path

### Memcached

Memcached binary file: */usr/bin/memcached*  
Memcached configuration file: */etc/sysconfig/memcached*  

### Other

no other components now

## Ports

These Ports is need when use Memcached, refer to [Safe Group Setting on Cloud Console](https://support.websoft9.com/docs/faq/tech-instance.html)

| Name | Number | Use |  Necessity |
| --- | --- | --- | --- |
| Memcached | 11211 | Remote connect Memcached | Optional |

## Version

You can see the version from product page of Marketplace. However, after being deployed to your server, the components will be automatically updated, resulting in a certain change in the version number. Therefore, the exact version number should be viewed by running the command on the server:

```shell
# Check all components version
sudo cat /data/logs/install_version.txt

# Linux Version
lsb_release -a

# Memcached Version
memcached -h
```