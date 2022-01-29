FROM debian:bullseye-slim

RUN apt-get update && \
    apt-get install -y wget && \
    wget https://github.com/prometheus/node_exporter/releases/download/v1.3.1/node_exporter-1.3.1.linux-amd64.tar.gz && \
    tar xf node_exporter-1.3.1.linux-amd64.tar.gz && \
    mv node_exporter-1.3.1.linux-amd64/node_exporter /bin/

EXPOSE      9100
USER        nobody
ENTRYPOINT  [ "/bin/node_exporter" ]
