FROM alpine:3.6
RUN sed -i "s|http://dl-cdn.alpinelinux.org|https://mirrors.ustc.edu.cn|g" /etc/apk/repositories &&\
    apk add --no-cache vim curl &&\
    rm -rf /var/lib/apt/lists/*
