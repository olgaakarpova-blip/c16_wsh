FROM ubuntu:22.04

RUN apt-get install openssh iproute2 curl bash sudo tcpdump shadow python3

COPY start.sh /usr/local/bin/start.sh
RUN chmod +x /usr/local/bin/start.sh

CMD ["/usr/local/bin/start.sh"]
