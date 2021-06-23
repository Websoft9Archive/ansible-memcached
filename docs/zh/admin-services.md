# 服务启停

使用由Websoft9提供的 Memcached 部署方案，可能需要用到的服务如下：  

### Memcached

```shell
sudo docker start memcached
sudo docker stop memcached
sudo docker restart memcached
sudo docker stats memcached
```

### Memcached-admin

```shell
sudo docker start memcached-admin
sudo docker stop memcached-admin
sudo docker restart memcached-admin
sudo docker stats memcached-admin
```

### Nginx

```shell
sudo systemctl start nginx
sudo systemctl stop nginx
sudo systemctl restart nginx
sudo systemctl status nginx
```

### Docker

```shell
sudo systemctl start docker
sudo systemctl restart docker
sudo systemctl stop docker
sudo systemctl status docker
```

### Docker-Compose
```
#创建容器编排
sudo docker-compose up -d

#删除容器编排
sudo docker-compose up -d

#启动/停止/重启
sudo docker-compose start
sudo docker-compose stop
sudo docker-compose restart
```