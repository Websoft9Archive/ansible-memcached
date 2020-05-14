# Update & Upgrade

Updates and upgrades are one of the maintenance tasks for system. Programs that are not upgraded for a long time, like buildings that are not maintained for a long time, will accelerate aging and gradually lose functionality until they are unavailable.

You should know the differences between the terms **Update** and **Upgrade**([Extended reading](https://support.websoft9.com/docs/faq/tech-upgrade.html#update-vs-upgrade))
- Operating system patching is **Update**, Ubuntu16.04 to Ubuntu18.04 is **Upgrade**
- MySQL5.6.25 to MySQL5.6.30 is **Update**, MySQL5.6 to MySQL5.7 is **Upgrade**

For Memcached maintenance, focus on the following two Update & Upgrade jobs

- Sytem update(Operating System and Running Environment) 
- Memcached upgrade 

## System Update

Run an update command to complete the system update:

``` shell
#For Ubuntu
apt update && apt upgrade -y

#For Centos&Redhat
yum update -y
```
> This deployment package is pre-configured with a scheduled task for automatic updates. If you want to remove the automatic update, please delete the corresponding Cron

## Memcached Upgrade

If you can't upgrade Memcached version you want by apt/yum, you can use the install from source for your upgrade

Refer to official docs: [Install from source](https://github.com/memcached/memcached/wiki/Install)