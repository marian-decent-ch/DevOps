# DevOps
Aim of the repository is to setup DevOps via Docker images as part of automated tools for DCore components: decentd, cli_wallet. Setup will offer one click tools for building binaries from source code, for creating actual snapshots, for deployment of private testnet, etc.

# Docker
## Decentd

Run DCore daemon in docker container:

docker run -it -p 8090:8090 -p 9090:9090 decentnetwork/decentd decentd
