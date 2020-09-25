FROM adoptopenjdk/openjdk15:x86_64-alpine-jre-15_36

RUN apk update \
    && apk upgrade \
    && apk add -y curl ca-certificates openssl git tar bash sqlite fontconfig \
    && adduser -D -h /home/container container

USER container
ENV  USER=container HOME=/home/container

WORKDIR /home/container

COPY /java-15/entrypoint.sh /entrypoint.sh

CMD ["/bin/bash", "/entrypoint.sh"]
