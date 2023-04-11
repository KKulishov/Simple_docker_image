FROM node:18.12

ENV LOCALTIME Europe/Moscow
RUN ln -snf /usr/share/zoneinfo/$LOCALTIME /etc/localtime && echo $LOCALTIME > /etc/timezone

RUN set -ex && \
    mkdir -p /app && \
    chown -R node:node /app && \
    chown node:node /app

WORKDIR /app

COPY .docker/back/docker-entrypoint.sh /entrypoint.sh

ENTRYPOINT ["/entrypoint.sh"]
