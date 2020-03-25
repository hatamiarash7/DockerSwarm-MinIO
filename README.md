![logo](logo.svg)
# Docker Swarm MinIO
 Deploy MinIO storage server in Docker Swarm

### Prerequisites

You should create your credentials keys. Run in master node :

```shell
echo "AKIAIOSFODNN7EXAMPLE" | docker secret create access_key -
echo "wJalrXUtnFEMI/K7MDENG/bPxRfiCYEXAMPLEKEY" | docker secret create secret_key -
```

We have 4 service by default that run in 4 node. Set label for Swarm nodes and configure them in `deploy > placement > constraints` and `environment > MINIO_DISTRIBUTED_NODES`

### Bringing up the stack

```shell
docker stack deploy -c docker-stack.yml MinIO
```

Wait until all disks are up and running then you can access MinIO cluster from exposed ports ( 9002-9005 ) and use any client to use them
