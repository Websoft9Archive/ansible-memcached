# Start or Stop the Services

These commands you must know when you using the Memcached of Websoft9

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
# Create Containers
sudo docker-compose up -d

# Remove Containers
sudo docker-compose down -v

sudo docker-compose start
sudo docker-compose stop
sudo docker-compose restart
```