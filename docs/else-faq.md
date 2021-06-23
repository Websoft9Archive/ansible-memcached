# FAQ

#### What is the Memcached client?

Memcached does not provide specific client. However, standard tools like telnet are enough to test container. Under Linux it is possible to connect by CLI command. We can invoke telnet from host machine, to connect to running Memcached server

#### Can I use `memcached -h` to configure Memcached?

No, this deployment use Docker for Memcached, if you want to configure Memcached, refer to [Commandline Arguments](/solution-cli.md#commandline-arguments)

#### Does Memcached need a password to log in?

No password authentication required

#### Is there a web-GUI tool for Memcached?

Yes

#### What's the difference between Deployment and Installation?

- Deployment is a process of installing and configuring a sequence of software in sequence in a different order, which is a complex system engineering.  
- Installation is the process of starting the initial wizard after the application is prepared.  
- Installation is simpler than deployment. 

#### What's Cloud Platform?

Cloud platform refers to platform manufacturers that provide cloud computing services, such as: **Azure, AWS, Alibaba Cloud, HUAWEI CLOUD, Tencent Cloud**, etc.

#### What is the difference between Instance, Cloud Server, Virtual Machine, ECS, EC2, CVM, and VM?

No difference, just the terminology used by different manufacturers, actually cloud servers