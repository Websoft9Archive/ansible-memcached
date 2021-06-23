# Troubleshooting

We collect the most common troubleshooting of using aaPanel for your reference:

> Many troubleshooting is closely related to the Server, if you can confirm troubleshooting is related to Cloud Platform, please refer to [Cloud Platform Documentation](https://support.websoft9.com/docs/faq/tech-instance.html)

#### Memcached service could not be started?

Insufficient disk space, insufficient memory, and configuration file errors can make Memcached service could not be started  

It is recommended to first check through the command.

```shell
# check logs
sudo docker log memcached

# view disk space
df -lh

# view memory rate
free -lh 

# view process
ps aux
```