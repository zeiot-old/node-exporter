# VERSION 0.13.0
# AUTHOR:         Nicolas Lamirault <nicolas.lamirault@gmail.com>
# DESCRIPTION:    zeiot/rpi-prometheus

FROM resin/armv7hf-debian:jessie
MAINTAINER Nicolas Lamirault <nicolas.lamirault@gmail.com>

ENV NODE_EXPORTER_VERSION 0.13.0

ADD https://github.com/prometheus/node_exporter/releases/download/v${NODE_EXPORTER_VERSION}/node_exporter-${NODE_EXPORTER_VERSION}.linux-armv7.tar.gz /node_exporter.tar.gz

RUN tar -xf /node_exporter.tar.gz && \
    rm /node_exporter.tar.gz && \
    mv node_exporter-${NODE_EXPORTER_VERSION}.linux-armv7/node_exporter /usr/bin/node_exporter && \
    rm -fr node_exporter-${NODE_EXPORTER_VERSION}.linux-armv7

EXPOSE     9100

ENTRYPOINT [ "/usr/bin/node_exporter" ]
