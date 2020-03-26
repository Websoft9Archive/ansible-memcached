# Memcached CLI

## About it

redis-cli is the Memcached command line interface, a simple program that allows to send commands to Memcached, and read the replies sent by the server, directly from the terminal.

It has two main modes: 
* an interactive mode where there is a REPL (Read Eval Print Loop) where the user types commands and get replies; 
* and another mode where the command is sent as arguments of redis-cli, executed, and printed on the standard output.

## Command line usage

| **Command** | **Description** |
| --- | --- |
| redis-benchmark | Performance test |
| SAVE | Backup Data |
| CONFIG GET dir | Restore Data |
| INFO | Manage Memcached services |

More details please read the official docs: https://redis.io/topics/rediscli