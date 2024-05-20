---
label: Docker
---

# Docker Installation

## With Docker compose
1. `git clone https://github.com/sillytavern/sillytavern`
2. `cd sillytavern/docker`
3. `docker compose up`
4. config & data @ docker directory
5. `docker compose up -d`

### Updating the container

1. pull latest images: `docker compose pull`
2. Restart the container: `docker compose up -d --remove-orphans`
3. Optionally, remove obsolete images: `docker image prune

## Without Docker compose

1. Pull the image from the container registry: `docker pull ghcr.io/sillytavern/sillytavern:latest`
2. prep dirs for config&data
3. `export STDIR="/home/heblushabus/ST/"`

4. `docker run --name sillytavern -d -p 8000:8000 -v $STDIR/config:/home/node/app/config -v $STDIR/data:/home/node/app/data  --restart always ghcr.io/sillytavern/sillytavern:release`
`