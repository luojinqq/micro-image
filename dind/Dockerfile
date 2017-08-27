FROM docker:dind
ENV version=v0.4.0
RUN sed -i "s|http://dl-cdn.alpinelinux.org|https://mirrors.ustc.edu.cn|g" /etc/apk/repositories \
    &&wget https://github.com/rancher/cli/releases/download/${version}/rancher-linux-amd64-${version}.tar.gz \
    &&tar -xvf rancher-linux-amd64-${version}.tar.gz \
    &&mv /rancher-${version}/rancher /bin
COPY cli.json /root/.rancher/cli.json
