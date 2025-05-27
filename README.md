# ダンボー

<p align="center">
<img src="https://github.com/Nathan-Yorio/danbo/blob/4f2ffc1264bc121fd881ff92dbd13ba6d8da7fae/assets/danbo-smol.png" width="150" height="150" />
</p>


Repository where I am storing
reproducible podman container
builds for use with distrobox.

- I pull them down like this
```
docker logout ghcr.io
podman logout ghcr.io
distrobox create -p -i ghcr.io/y0ri0/dev:latest --name devbox --hostname box
```

Named Danbo after [Danbo](https://en.wikipedia.org/wiki/Danbo_(character))
