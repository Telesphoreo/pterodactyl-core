FROM openjdk:15-slim

RUN apt update \
    && apt upgrade \
    && apt install -y curl ca-certificates openssl git tar bash sqlite fontconfig \
    && adduser -D -h /home/container container

USER container
ENV  USER=container HOME=/home/container

WORKDIR /home/container

COPY /java-15/entrypoint.sh /entrypoint.sh

CMD ["/bin/bash", "/entrypoint.sh"]
