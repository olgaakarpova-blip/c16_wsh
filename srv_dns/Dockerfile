FROM ubuntu:22.04

ENV DEBIAN_FRONTEND=noninteractive TZ=Etc/UTC

RUN apt-get update \
 && apt-get install -y --no-install-recommends \
    iproute2 \
    bash \
    curl \
    sudo \
    openssh-server \
    ca-certificates \
    python3 \
    wget \
 && rm -rf /var/lib/apt/lists/*

RUN wget https://github.com/coredns/coredns/releases/download/v1.13.2/coredns_1.13.2_linux_amd64.tgz \
 && tar xvf coredns_1.13.2_linux_amd64.tgz \
 && sudo mv coredns /usr/local/bin/

COPY start.sh /start.sh
RUN chmod +x /start.sh

ENTRYPOINT ["/start.sh"]
