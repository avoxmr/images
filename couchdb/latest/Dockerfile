FROM    --platform=$TARGETOS/$TARGETARCH couchbase:latest

LABEL   author="MrAvox" maintainer="mravox@proton.me"

ENV     DEBIAN_FRONTEND noninteractive

RUN     apt update && \
        apt -y upgrade && \
        apt -y install iproute2 && \
        useradd -m -d /home/container container

USER    container
ENV     USER=container HOME=/home/container
WORKDIR /home/container

ENTRYPOINT []
COPY    ./entrypoint.sh /entrypoint.sh
CMD     ["/bin/bash", "/entrypoint.sh"]
