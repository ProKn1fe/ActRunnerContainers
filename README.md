# Containers images for Gitea Actions act_runner.

### The problem
As you probably know by default Gitea act_runner uses [16-bullseye](https://hub.docker.com/layers/library/node/16-bullseye/images/sha256-59167f718a1f6daecb900ffbb4f5b09f0dca709c5d7e180f33bbaeac076cdb7b?context=explore) docker images for `ubuntu-latest` tag because to run action `node` is required to be installed inside container and for some reasons canonical and node don't provide ubuntu images with preinstalled node.

### The solution
This repository xd.

### How to use:

In config.yml we can set docker imgaes manually, for example:
```
labels: [ubuntu-latest:docker://act-runner-containers:focal, ubuntu-23.04:docker://act-runner-containers:lunar]
```
You can set system name by code name `lunar` or just by version number `23.04`.

Images list:
* Ubuntu 20.04 (focal)
* Ubuntu 22.04 (jammy)
* Ubuntu 23.04 (lunar)
* Ubuntu 23.10 (mantic)
* Ubuntu 24.04 (noble)
