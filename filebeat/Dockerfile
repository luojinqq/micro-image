FROM docker.source3g.com:5000/env/filebeat
ENV LANG="zh_CN.UTF-8"
RUN yum install -y vim
COPY filebeat.tmpl /etc/filebeat/
CMD dockerize -template filebeat.tmpl:filebeat.yml filebeat
