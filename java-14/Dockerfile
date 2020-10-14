FROM adoptopenjdk/openjdk14-openj9:alpine-jre

RUN apk update \
    && apk upgrade \
    && apk add curl ca-certificates openssl git tar bash sqlite fontconfig tzdata iproute2 \
    && adduser -D -h /home/container container

USER container
ENV  USER=container HOME=/home/container

WORKDIR /home/container

COPY /java-14/entrypoint.sh /entrypoint.sh

CMD ["/bin/bash", "/entrypoint.sh"]
