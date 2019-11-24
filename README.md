# dockerd-exporter

Prometheus exporter for Docker daemon metrics


## Requirements

You must enable Docker experimental metrics-addr in all Swarm nodes.

Edit `/etc/docker/daemon.json` to add these properties:
```
{
	...
	"experimental": true,
	"metrics-addr": "0.0.0.0:9323"
}
```

Don't forget to restart Docker daemon with `systemctl restart docker` (do it for every Swarm node).
