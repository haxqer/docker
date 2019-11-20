# ------------------------------------------------------------------------------------
# @build-example docker build . -f Dockerfile -t haxqer/nginx:yml
#
FROM nginx:latest



RUN apt-get update \
        && apt-get install -y \
            curl \
    && apt-get clean \
    && apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false

RUN curl -k -o /etc/nginx/conf.d/default.conf http://raw.githubusercontent.com/haxqer/docker/master/nginx/yml/default.conf -L


