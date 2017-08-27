FROM alpine:3.6

ENV DOCKERIZE_VERSION v0.2.0

RUN sed -i "s|http://dl-cdn.alpinelinux.org|https://mirrors.ustc.edu.cn|g" /etc/apk/repositories
RUN set -x; \
    apk add --no-cache bash vim curl tar openssl openssl-dev ca-certificates \
    &&wget https://github.com/jwilder/dockerize/releases/download/$DOCKERIZE_VERSION/dockerize-linux-amd64-$DOCKERIZE_VERSION.tar.gz \
    && tar -C /bin -xzvf dockerize-linux-amd64-$DOCKERIZE_VERSION.tar.gz