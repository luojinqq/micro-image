from microimages/alpine

maintainer jimluo <luojin@guoshengtianfeng.com>

label service=jre

env LANG en_US.UTF-8
env JAVA_VERSION 7.91
env JAVA_APK_VERSION 7.91
RUN sed -i "s|http://dl-cdn.alpinelinux.org|https://mirrors.ustc.edu.cn|g" /etc/apk/repositories

run apk add --update openjdk7-jre="$JAVA_APK_VERSION" &&\
    apk add vim

env JAVA_HOME /usr/lib/jvm/default-jvm

workdir /app