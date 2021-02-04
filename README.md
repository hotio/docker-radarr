[<img src="https://hotio.dev/img/radarr.png" alt="logo" height="130" width="130">](https://github.com/Radarr/Radarr)

[![GitHub Source](https://img.shields.io/badge/github-source-ffb64c?style=flat-square&logo=github&logoColor=white&labelColor=757575)](https://github.com/hotio/radarr)
[![GitHub Registry](https://img.shields.io/badge/github-registry-ffb64c?style=flat-square&logo=github&logoColor=white&labelColor=757575)](https://github.com/orgs/hotio/packages/container/package/radarr)
[![Docker Pulls](https://img.shields.io/docker/pulls/hotio/radarr?color=ffb64c&style=flat-square&label=pulls&logo=docker&logoColor=white&labelColor=757575)](https://hub.docker.com/r/hotio/radarr)
[![Discord](https://img.shields.io/discord/610068305893523457?style=flat-square&color=ffb64c&label=discord&logo=discord&logoColor=white&labelColor=757575)](https://hotio.dev/discord)
[![Upstream](https://img.shields.io/badge/upstream-project-ffb64c?style=flat-square&labelColor=757575)](https://github.com/radarr/radarr)
[![Website](https://img.shields.io/badge/website-hotio.dev-ffb64c?style=flat-square&labelColor=757575)](https://hotio.dev/containers/radarr)

## Starting the container

CLI:

```shell
docker run --rm \
    --name radarr \
    -p 7878:7878 \
    -e PUID=1000 \
    -e PGID=1000 \
    -e UMASK=002 \
    -e TZ="Etc/UTC" \
    -e ARGS="" \
    -v /<host_folder_config>:/config \
    hotio/radarr
```

Compose:

```yaml
version: "3.7"

services:
  radarr:
    container_name: radarr
    image: hotio/radarr
    ports:
      - "7878:7878"
    environment:
      - PUID=1000
      - PGID=1000
      - UMASK=002
      - TZ=Etc/UTC
      - ARGS
    volumes:
      - /<host_folder_config>:/config
```

In most cases you'll need to add additional volumes, depending on your own personal preference, to get access to your files.

## Tags

Go [here](https://hotio.dev/tags-overview/#hotioradarr) to see all available tags.
