# rabbitmq-lab
RabbitMQ LAB in Docker

The setup needs to create the .erlang.cookie file in the directory but the permission needs to be RW of for owner (uses sudo to change it):
```
-rw------- 1 systemd-coredump root 41 Apr  6 15:02 .erlang.cookie
```

File content is a huge toke :D

PS.: this Docker setup store the RabbitMQ structured data of each cluster container into ./storage directory.
The setup uses the `cluster_formation.peer_discovery_backend = classic_config` so after the first startup, if the cluster fail to detect all nodes, remove the storage directory and retry.
