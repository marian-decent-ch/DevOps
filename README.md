# DevOps
Aim of the repository is to setup DevOps via Docker images as part of automated tools for DCore components: decentd, cli_wallet. Setup will offer one click tools for building binaries from source code, for creating actual snapshots, for deployment of private testnet, etc.

# Docker
In order to run containers, docker engine must be installed.

## Install
Download and install Docker engine from [store](https://store.docker.com/search?type=edition&offering=community)

or directly

### MacOS
[DockerCE](https://download.docker.com/mac/stable/Docker.dmg)

### Windows
[DockerCE](https://download.docker.com/win/stable/Docker%20for%20Windows%20Installer.exe)

### Linux
Run as root:

```
curl -fsSL https://get.docker.com/ | sh
```

## Decentd

Run DCore daemon in docker container:
```
docker run -it -p 8090:8090 -p 9090:9090 decentnetwork/decentd decentd
```


## CLI_wallet

Run DCore wallet in docker container:
```
docker run -it -p 8090:8090 -p 8092:8092 decentnetwork/cli_wallet cli_wallet
```
