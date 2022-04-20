# Docker Swarm MinIO

![logo](logo.svg)

Deploy MinIO storage server in Docker Swarm

## Prerequisites

You should create your credentials keys. Run in master node :

```shell
echo "AKIAIOSFODNN7EXAMPLE" | docker secret create access_key -
echo "wJalrXUtnFEMI/K7MDENG/bPxRfiCYEXAMPLEKEY" | docker secret create secret_key -
```

We have 4 service by default that run in 4 node. Set label for Swarm nodes and configure them in `deploy > placement > constraints` and `environment > MINIO_DISTRIBUTED_NODES`

## Bringing up the stack

```shell
docker stack deploy -c docker-stack.yml MinIO
```

Wait until all disks are up and running then you can access MinIO cluster from exposed ports ( 9002-9005 ) and use any client to use them

---

## Support

[![Donate with Bitcoin](https://en.cryptobadges.io/badge/micro/3GhT2ABRuHuXGNzP6DH5KvLZRTXCBKkx2y)](https://en.cryptobadges.io/donate/3GhT2ABRuHuXGNzP6DH5KvLZRTXCBKkx2y) [![Donate with Ethereum](https://en.cryptobadges.io/badge/micro/0x4832fd8e2cfade141dc4873cc00cf77de604edde)](https://en.cryptobadges.io/donate/0x4832fd8e2cfade141dc4873cc00cf77de604edde)

[![ko-fi](https://www.ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/D1D1WGU9)

<div><a href="https://payping.ir/@hatamiarash7"><img src="https://cdn.payping.ir/statics/Payping-logo/Trust/blue.svg" height="128" width="128"></a></div>

## Contributing

Don't be shy to be a contributor 😉

1. Fork it !
2. Create your feature branch : `git checkout -b my-new-feature`
3. Commit your changes : `git commit -am 'Add some feature'`
4. Push to the branch : `git push origin my-new-feature`
5. Submit a pull request

## Issues

Each project may have many problems. Contributing to the better development of this project by reporting them.
