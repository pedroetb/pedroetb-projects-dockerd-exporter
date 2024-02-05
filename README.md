# dockerd-exporter

Prometheus exporter for Docker daemon metrics

## Requirements

You must enable Docker `metrics-addr` in all Swarm nodes.

Edit `/etc/docker/daemon.json` to add `"metrics-addr": "0.0.0.0:9323"` property:

> Note: if your nodes are using Docker with version `< v20.10`, you must add `experimental: true` property too.

Don't forget to restart Docker daemon with `systemctl restart docker` (do it for every Swarm node).
