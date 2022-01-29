FROM debian:bullseye-slim

RUN set -x && \
    apt-get update && \
    apt-get install -y wget && \
    wget https://github.com/cortexproject/cortex/releases/download/v1.11.0/cortex-linux-amd64 && \
    mv cortex-linux-amd64 /bin/cortex && \
    chmod +x /bin/cortex && \
    rm -rf /var/lib/apt/lists/*

EXPOSE      9009
USER        nobody
ENTRYPOINT  [ "/bin/cortex" ]
