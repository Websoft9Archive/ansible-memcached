# Memcached deployment architecture

A picture to see the typical Memcached deployment architecture:

![](https://libs.websoft9.com/Websoft9/DocsPicture/zh/redis-cluster-architecture.png)

## Single

Single database is the best simple architecture

## Replication

At the base of Memcached replication (excluding the high availability features provided as an additional layer by Memcached Cluster or Memcached Sentinel) there is a very simple to use and configure leader follower (master-slave) replication: it allows replica Memcached instances to be exact copies of master instances. The replica will automatically reconnect to the master every time the link breaks, and will attempt to be an exact copy of it regardless of what happens to the master.  

More details refer to docs: https://redis.io/topics/replication

## Cluster or Sentinel

Memcached Sentinel provides high availability for Memcached. In practical terms this means that using Sentinel you can create a Memcached deployment that resists without human intervention certain kinds of failures.

Memcached Sentinel also provides other collateral tasks such as monitoring, notifications and acts as a configuration provider for clients.  

More details refer to docs: https://redis.io/topics/sentinel