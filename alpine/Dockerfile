FROM alpine:3.12

ENV LANG=C.UTF-8

RUN set -euxo pipefail \
    && echo 'https://mirrors.cloud.tencent.com/alpine/v3.12/main/' > /etc/apk/repositories \
    && echo 'https://mirrors.cloud.tencent.com/alpine/v3.12/community/' >> /etc/apk/repositories \
    && apk update \
    && apk add --no-cache tzdata bash curl busybox-extras \
    && cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime && echo Asia/Shanghai > /etc/timezone \
    && apk del tzdata 
