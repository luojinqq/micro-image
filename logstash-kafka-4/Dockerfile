FROM logstash:5-alpine

ONBUILD RUN sed -i "s|http://dl-cdn.alpinelinux.org|http://mirrors.aliyun.com|g" /etc/apk/repositories
RUN apk add --no-cache --virtual .build-deps \
        curl ruby ruby-bundler
#RUN bundle config mirror.https://rubygems.org https://ruby.taobao.org
ONBUILD RUN sed 's#^source.*#source "https://ruby.taobao.org/"#' /usr/share/logstash/Gemfile -i
ONBUILD RUN gem sources --remove https://rubygems.org/
ONBUILD RUN gem sources -a https://ruby.taobao.org/
ONBUILD RUN gem sources -l
#RUN gem install rails -V

RUN /usr/share/logstash/bin/logstash-plugin uninstall logstash-input-kafka\
    &&/usr/share/logstash/bin/logstash-plugin install --version 4.2.0 logstash-input-kafka
RUN /usr/share/logstash/bin/logstash-plugin uninstall logstash-input-kafka\
    &&/usr/share/logstash/bin/logstash-plugin install --version 4.2.0 logstash-output-kafka
#ADD logstash-input-kafka-4.2.0 /usr/share/logstash/logstash-input-kafka-4.2.0