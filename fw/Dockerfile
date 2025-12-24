FROM ubuntu:22.04

ENV DEBIAN_FRONTEND=noninteractive \
    TZ=Etc/UTC


RUN apt-get update \
 && apt-get install -y \
    iproute2 \
    iptables \
    nftables \
    openssh-server \
    openssh-client \
    sudo \
    bash \
    tcpdump \
    nano \
    python3 \
    passwd \
    util-linux \
    login \
    uidmap \
 && rm -rf /var/lib/apt/lists/*

COPY start.sh /usr/local/bin/start.sh
RUN chmod +x /usr/local/bin/start.sh

CMD ["/usr/local/bin/start.sh"]
