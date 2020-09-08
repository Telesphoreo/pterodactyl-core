FROM adoptopenjdk/openjdk8-openj9:debian-slim

RUN apt update \
    && apt upgrade -y \
    && apt install -y curl ca-certificates openssl git tar bash sqlite fontconfig \
    && adduser -D -h /home/container container

USER container
ENV  USER=container HOME=/home/container

WORKDIR /home/container

COPY entrypoint.sh /entrypoint.sh

CMD ["/bin/bash", "/entrypoint.sh"]
