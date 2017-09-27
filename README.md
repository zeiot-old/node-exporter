# RPI Prometheus node exporter

* Master : [![pipeline status](https://gitlab.com/zeiot/rpi-node_exporter/badges/master/pipeline.svg)](https://gitlab.com/zeiot/rpi-node_exporter/commits/master)

Docker image of [Prometheus node exporter][] to use on a [Raspberry PI][].

Configure binfmt-support on the Docker host (works locally or remotely, i.e: using boot2docker):

    $ docker run --rm --privileged multiarch/qemu-user-static:register --reset

Then you can run an armhf image from your x86_64 Docker host :

    $ make run version=1.0

Or build :

    $ make build version=1.0


# Supported tags

* [![](https://images.microbadger.com/badges/version/zeiot/rpi-node_exporter:0.13.0.svg)](https://microbadger.com/images/zeiot/rpi-node_exporter:0.13.0 "Get your own version badge on microbadger.com")
* [![](https://images.microbadger.com/badges/version/zeiot/rpi-node_exporter:0.12.0.svg)](https://microbadger.com/images/zeiot/rpi-node_exporter:0.12.0 "Get your own version badge on microbadger.com")


## License

See [LICENSE](LICENSE) for the complete license.


## Changelog

A [ChangeLog.md](ChangeLog.md) is available.


## Contact

Nicolas Lamirault <nicolas.lamirault@gmail.com>


[Raspberry PI]: https://www.raspberrypi.org/
[Prometheus node exporter]: https://github.com/prometheus/node_exporter
