# Containers images for Gitea Actions act_runner.
![Docker Pulls](https://img.shields.io/docker/pulls/prokn1fe/act-runner-containers)

### The problem.
As you probably know by default Gitea act_runner uses [16-bullseye](https://hub.docker.com/layers/library/node/16-bullseye/images/sha256-59167f718a1f6daecb900ffbb4f5b09f0dca709c5d7e180f33bbaeac076cdb7b?context=explore) docker images for `ubuntu-latest` label because to run actions - `node` is required to be installed inside container and for some reasons Canonical and node don't provide ubuntu images with preinstalled node.

### The solution.
This repository xd.

### How to use:

In config.yaml we can set docker imgaes manually, for example:
```
labels: [ubuntu-latest:docker://act-runner-containers:focal, ubuntu-23.04:docker://act-runner-containers:lunar]
```
You can set system name by code name `lunar` or just by version number `23.04`.

Images list:
| OS | Version | Code name | Tag | Stats |
|----|---------|-----------|-----|-------|
| Ubuntu | 20.04 | Focal | act-runner-containers:focal | ![focal](https://img.shields.io/docker/image-size/prokn1fe/act-runner-containers/focal) |
| Ubuntu | 22.04 | Jammy | act-runner-containers:jammy | ![focal](https://img.shields.io/docker/image-size/prokn1fe/act-runner-containers/jammy) |
| Ubuntu | 23.04 | Lunar | act-runner-containers:lunar | ![focal](https://img.shields.io/docker/image-size/prokn1fe/act-runner-containers/lunar) |
| Ubuntu | 23.10 | Mantic | act-runner-containers:mantic | ![focal](https://img.shields.io/docker/image-size/prokn1fe/act-runner-containers/mantic) |
| Ubuntu | 24.04 | Noble | act-runner-containers:noble | ![focal](https://img.shields.io/docker/image-size/prokn1fe/act-runner-containers/noble) |
